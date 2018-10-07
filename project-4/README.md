# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Kaggle Competition - Starter
https://www.kaggle.com/c/predict-west-nile-virus/submissions?sortBy=date&group=all&page=1
## Introduction

Our task is to predict West Nile occurances based on data provided from previous years of occuance in the Chicago area.

## Dataset

Our data contained trap collection information for 2007,200,2011, and 2013. We focused on creating predictions around two main areas:

- Dependency on seasonal variation
- Species type
- Location of Trap
- Rolling Weather data
- Spatial Analysis of traps to L-Train stop


#### Navigating Group Work

Logistic Regression:

- Logisitic Regression is allowing feature addition to be reflected well in the data. Probabilities are lower range than other model types by produce better roc auc scores.

SVC:

- The SVC model seems to have peaked lower than what our Logisitc regression. Would need to create more features that SVC can divide on.

## Deliverables

Here is a guide to our Deliverables

## Scores

1. Jerome has an SVM model that scored 0.71993 on kaggle (ROC AUC of test set)
2. Conor has Logistic Regression model that scored .64 on Kaggle. Includes seasonal probability adjustments and normalized X.
3. Conor has Logistic Regression model that scored .74 on Kaggle. 2 week rolling weather. YearDay included as model feature.
4. Conor has dumb submission that scored .62. Used seasonal probabilities only.
5. (9/20) James has Logistic Regression model score a 0.766 on Kaggle. Optimized weather, YearDay included, Pipens dummy dropped.
6. (9/22) James used a Log Reg with L_train stops for a score of 0.774 on Kaggle.

## Presentation

https://docs.google.com/presentation/d/1UpYyo-0XNsWwuhoMRPJfuZUvaza92SpWuIGKqrGs_5w/edit?usp=sharing
