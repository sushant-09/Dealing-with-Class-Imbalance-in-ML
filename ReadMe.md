# Dealing with Class Imbalance in Machine Learning
## Problem Statement
Most existing classification approaches assume the underlying training set is
evenly distributed but many real-world classification problems have an imbalanced class distribution, such as rare disease identification, fraud detection, spam detection, churn prediction, electricity theft & pilferage etc.
These types of problems are also known as rare event prediction or extreme event prediction.
##### Class Imbalance
The training set for one class (majority) far surpasses the training set of the other class (minority), in which, the minority class is often the more interesting class.

## Scope of the project
In this project we,
- Review the issues that come with learning from imbalanced data sets and various problems in class-imbalance classification.
- Discuss some data level as well as algorithm level approaches for rare event prediction.



## Issues with imbalanced datasets
- Most standard algorithms are accuracy driven, however, in a class imbalance dataset, accuracy tells very little about the minority class.
- Lack of information caused by small sample size.
##### Why accuracy is a bad metric?
- Suppose class A is 99% of our data-set and class B is the other 1%, but we are most interested in identifying instances of class B.
- We can reach an accuracy of 90% by simply predicting class A every time, but this provides a useless classifier for our intended use case.
- Instead, a properly calibrated method may achieve a lower accuracy, but would have a substantially higher true positive rate (or recall), which is really the metric we want to optimize for.

Generally, this problem deals with the trade-off between recall (percent of truly positive instances that were classified as such) and precision (percent of positive classifications that are truly positive).

## Dataset Description
We have chosen a dataset that contains transactions made by credit cards in September 2013 by European cardholders.
- This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions.
- The dataset is highly imbalanced, the positive class (frauds) account for 0.172% of all transactions.
- It contains only numerical input variables which are the result of a PCA transformation (due to confidentiality issues).
- Feature 'Class' is the response variable, and it takes value 1 in case of fraud and 0 otherwise.


## Data level approaches
- Undersampling (RUS)
- Oversampling (SMOTe)
## Algorithm level approaches
- Cost Sensitive Learning
- Ensemble Learning
- One Class Learning
- Hybrid Methods
## Models were evaluated on the following metrics
- Recall of the minority class
- ROC_AUC score
- F1-Score
- Precision