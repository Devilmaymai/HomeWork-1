# HomeWork-1

## Part2:

database: https://www.kaggle.com/ronitf/heart-disease-uci 

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

### 分析與說明
#### 年齡與性別：

一開始先針對資料對象的年齡及性別組成做基本的分析。
針對年齡組成選用的是長條圖，而性別組成則選用圓餅圖作呈現。

由所做出來的初步分析可以看見，在有心臟病與沒有心臟病的資料中，年齡及性別的組成是有一定程度上的差異。
因此，這兩的因子在training上或許能當不錯的決策點。

但在實際上的臨床分析方面，則代表著後續在分析心臟病與沒有心臟病的資料時，可能需要將會受這兩個因素影響的資料做一點修正，才能避免bias的情形。

