# HomeWork-1

## Part1:

### 1:

![](https://imgur.com/uz8fdX9.png)

### 2:

![](https://imgur.com/MX5byNC.png)

### 3:

![](https://imgur.com/bzWh3m5.png)

### 4:

![](https://imgur.com/VbZNV58.png)

### 5:

![](https://imgur.com/cbSbNqk.png)

## Part2:

dataset: https://www.kaggle.com/ronitf/heart-disease-uci 

連結中的data總共有14個屬性。

在這裡的分析我只選用其中7種屬性(age、sex、trestbps、chol、thalach、oldpeak、target)做分析。

其中sex與target為類別型數據，而其他5種為數字型數據。

age: 年齡

sex: 性別

trestbps: 休息時血壓

chol: 膽固醇濃度(mg/dl)

thalach: 最大心律

oldpeak: ST segment (心臟早期的再極化) 由運動所導致的改變(相較於靜止時)

target: 確診心臟病與否

<br>

### 分析與說明
#### 年齡與性別：

一開始先針對資料對象的年齡及性別組成做基本的分析。
針對年齡組成選用的是長條圖，而性別組成則選用圓餅圖作呈現。

![](https://imgur.com/9NAFPFS.png)
![](https://imgur.com/aWibsI6.png)
![](https://imgur.com/okbzik2.png)
![](https://imgur.com/0AKg1vn.png)

由所做出來的初步分析可以看見，在有心臟病與沒有心臟病的資料中，年齡及性別的組成是有一定程度上的差異。
因此，這兩的因子在training上或許能當不錯的決策點。

但在實際上的臨床分析方面，則代表著後續在分析心臟病與沒有心臟病的資料時，可能需要將會受這兩個因素影響的資料做一點修正，才能避免bias的情形。

舉例來說，兩群資料在血壓高低方面可能沒有明顯差異，但年齡組成卻明顯不同。此時若使用年齡normalize後，可能就能看到不同結果。

<br>

#### trestbps等因素與心臟病的關聯：

接下來，我將age、trestbps、chol、thalach、oldpeak等數據型數據，與有心臟病與否做Heatmap分析。
在這裡我把Heart disease的positive (target = 1) 或 negative (target = 0)當作一的陽春的線性數據。

![](https://imgur.com/lNp3hzB.png)
![](https://imgur.com/rG8xmUw.png)

由所得的heat map可以看出thalach(最大心律)有較明顯的正相關，而oldpeak(心臟早期的再極化)有較明顯的負相關。
此外也可以看到age與trestbps、chol、thalach、oldpeak都有一定程度的相關性。這代表著，這些數據若能經過年齡的normalize，會比較好進行後續的分析。

<br>

#### 用BoxPlot分析Heart Disease(HD) positive or negative的組成：

在這裡將HD positive及negative在age、trestbps、chol、thalach、oldpeak等數據的組成，利用boxplot作分析。
可以看到兩組的數據outlier都有不少(在這樣的數據數之下)，也因此，除了前述normalize的處理，也還需進一步檢視outlier，才能進行分析。

![](https://imgur.com/wuEValV.png)
![](https://imgur.com/4tv4MMU.png)
![](https://imgur.com/rLJTYT0.png)
![](https://imgur.com/DkuYEwo.png)
![](https://imgur.com/N78XRIb.png)

<br>

### 結論

這個dataset的數據，若要進行有效的分析，還須更多更進一步的數據處理。
而若要直接拿來做training可能會由於bias的因素，得到較奇怪的結果，或是不易做不出較佳的結果。
由於目前尚在摸索在python上做分析的方法，因此這部分的作業就先停在這邊。

