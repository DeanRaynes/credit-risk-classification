# credit-risk-classification
Project for using and evaluating supervised learning models against credit worthiness of borrowers 

# Module 12 Report
## Overview of Analysis

* The purpose of this analysis is to determine if we can train a ML Model against our dataset to predict if the outstanding loans are healthy or high-risk. 
* The dataset we were using to make these predictions is based on the outstanding loans, data points included loan size, interest rate, borrower income, total num of accounts, total debt, debt to income ration, and if the loan had any derogatory marks.  By using this data that we have about the loan, borrower, and a pre-defined label of healthy vs high-risk loans, we were aiming to predict whether a loan would be healthy or high-risk. 
* The difference between a healthy loan and a high-risk loan would help indicate if the burrower may be more likely to default on their loan.  Which could help determine if any future loans should be given to the borrower.
* The stages of the ML process are as follows, first you need to split apart your target data from the rest of the dataset, this is your y axis. Next you run a train test split function using sklearn that will split your data into 2 chunks, training data that is 75% of the dataset, and testing data that is the remaining 25% of the dataset.  Next you choose the model you want to train your data with, in this case we choose the Logistic Regression model from sklearn.  You will fit the model to your train data.  Once you have done this step you can begin using the predict to determine how well the model has learned the dataset.  By running the predict against your test dataset you an run the classification report to see how well your model did at predicting the target. 

## Results

* Machine Learning Model 1:
     *          precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384

* The logistical regression model results as shown above provide an accuracy score of 99%, which is a good overall outcome.  However looking at the precision score per individual target we can see that the model is much better at providing a precise prediction of the 0 (healthy loans) target and not as good at the precision prediciton of the 1 (high-risk loan) target.  For the recall score, the model again was very good at recall of the 0 target and less so on the recall of the 1 target.

## Summary

* To summarize, if we are trying to predict the healthy loans this is a great model to utilize, but since we would rather predict the high-risk loans I would adjust the dataset to have more high-risk loans as a total of the dataset.  After running the dataset against the Random Forest and the KNN models, I feel that the Logistics Regression model is as good as if not a little bit better at predicting the high-risk loans.  The recall value using the KNN model is a bit better but the overall accuarcy nor the f1 score is any better then the logistic regression.  I would suggest the next step is to adjust the dataset being used to show a better representation of the high-risk loans.   
