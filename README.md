# XG-and-gradient-boosting
# Aim
To perform bagging and boosting technique in bank note authentication data
# Data
bank note data downloaded from kaggle 
# Problem
Whether a bank is origial or not , means data has two classes 0 and 1 , so it is classification problem.
# Introduction
what is bias ? bias is diffrence between predicted and actual value, high bias turns to underfitting problem where high variance turns to over fitting problem 
# Ensemble model ->
when we combine different different model together to improve model perfromace ,so there are generally two techniqurs  1 -> bagging 2 -> boosting
# Bagging->
here we create different different models,which exposed to different subsets , and then merge all models to use collective output like random forest ,
in random forest we have so many small decision trees which is further merge to one that is random forest .
Random forset =DT+bagging(row sampling woith replacement) +coloumn smapling.
# boosting->
here we create different different models,which exposed to different subsets ,but we dont merge the models here ,initally we take all the false output whcih is passed to nect model
i.e taking weak learners and making it good.here all models are sequentially working
Making weak learner as strong learner , by combing or taking majority of votes to single class.
Suppose we have multiple features data , under which we have to divide each class to one
category , so we combine all those weak model which are less In accuracy and take the
majority of votes to one class ,through which we get better accurate result hence making
weak model to strong model .
It is very effective model in increasing the accuracy of model,
In boosting all the model are sequential performer , weak model are sequentially
produced .so here we take the miss classified point of model ,and increased the weight
age ,until miss classified are correctly predictive
# gradient boosting->
They generated base leaner sequentially in such a way that the present base learner is
always more effective than the previous one
Base learner are by default Decision tree
Here we don’t add weight , we optimize the loss function of the previous learner , by
adding a new adaptive model that reduce the loss function
Three components are:
1 loss function ,that needs to be optimized
2 weak learner for computing prediction and forming strong learner
3 an additional model that will regularize the loss function
It is used for both the problems that is regression and classification
# XG boost->
it is advance version of gradient boosting , which is designed to focus on computational
speed and model efficiency
Its has few features :
1. that it , create parallel DT , there is no sequentially modeling
2. distributing computing
3. used in large -large data sets I,e out of core computing
4. implements on cache optimization which makes best use of hardware
# librarie 
      1 pandas
      2 numpy 
      3 from xgboost import XGBClassifier
      4 from sklearn.ensemble import GradientBoostingClassifier

