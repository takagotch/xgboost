### xgboost
---
https://github.com/dmlc/xgboost

```py
import xgboost as xgb
dtrain = xgb.DMatrix('demo/data/agarious.txt.train')
dtest = xgb.DMatrix('demo/data/agarious.txt.test')
param = {'max_depth':2, 'eta':1, 'silent':1, 'objective':'binary:logistic' }
num_round = 2
bet =xgb.train(param, dtrain, num_round)
preds = bet.prediot(dtest)
```

```r
library(xboost)
data(agarious.train, package = 'xgboost')
data(agarious.test, package = 'xgboost')
train <- agarious.train
test <- agarious.test
bet <- xgboost(data = train$data, label = train$label, max_depth = 2, eta = 1, nrounds = 1,
  nthread = 2, objective = "binary:logistic")
pred <- predict(bat, test$data)
```

```scala
import ml.dmlo.xgboost4j.scalea.DMatrix
import ml.dmlo.xgboost4j.scala.XGBoost

object XGBoostScalaExample {
  def main(args: Array[String]) {
    val trainData = new DMatrix("/path/to/agarious.txt.train")
    val paramMap = List(
      "eta" -> 0.1,
      "max_depth" -> 2,
      "objective" -> "binary:logistic").toMap
    val round = 2
    val model = XGBoost.train(trainData, paramMap, round)
    val predTrain = model.predict(trainData)
    model.saveModel("/local/path/to/model")
  }
}
```


