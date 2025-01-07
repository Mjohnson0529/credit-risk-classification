# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

## Overview of the Analysis

The purpose of this analysis was to determine the likihood a borrower would default on a loan they have taken out. The data used to make these predictions was: loan size, interest rate, borrower income, debt to income ratio, num of accounts, derogatory marks, total debt, loan status. This data was used too predict whether or not a borrower would pay back their loan or not. The variable we were tring to predict was the loan status. Meaning that we were trying to predict whether or not the borrower would default on their loan. To get this information, the data was split to remove the loan status column so it could be saved as a separate data frame to be used as labels. After this, the data features were split into training data and testing data. A Logistic Regression model was used to score the model. The model was then used to predict the test data and develop a balanced accuracy score, confusion matrix, and a classification report.

## Results

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores. 
    *              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.94      0.89       619

    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
weighted avg       0.99      0.99      0.99     19384

* Looking at the classification report we can see that the models accuracy is .99. 
    * This means that 99% of all the classifications were correct, whether they were positive or negative. 
* For the precision, we can see the score for the healthy loans is 100%. 
    * This means that 100% of the positive predictions that were made were correct. 
    * Similarly, 84% of the positive predictions that were made for the high risk loans were correct.
* For the recall, we can see that the healthy loans also scored better than the high risk loans.
    * For the healthy loans 99% of the correct positive predictions were actual positives
    * For the high risk loans 94% of the correct positive predictions were actual positives

## Summary

 The linear regression model does a very good job of accurately predicting both the healthy and high-risk loans chance of defaulting. The model does a little bit of a better job at predicting the chance of defaulting on healthy loans rather than the high-risk loans. This can be seen in the difference in precision and recall between the the two. We must also take in to consideration that in this situation the models performance is based on how well it can predict a high risk loan. This is because a lenders biggest concern is whether or not a borrow can pay back their loan, or in other words, they are a high risk. However, with a recall of .99 and .94, we can make the conclusion that this model is very reliable. 
