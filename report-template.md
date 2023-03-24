# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

Use Python to build a Supervised Machine Learning (SML) model that can identify and predict the creditworthiness of borrowers to evaluate loan risk with a high degree of accuracy.

* Explain what financial information the data was on, and what you needed to predict.

The data analystics used were: 
- Loan Size
- Interest Rate
- Borrower Income
- Debt to Income
- Number of Accounts
- Derogatory Marks
- Total Debt

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

Split the Data into Training and Testing Sets
- Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
- Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
- Split the data into training and testing datasets by using train_test_split.

Create a Logistic Regression Model with the Original Data
- Fit a logistic regression model by using the training data (X_train and y_train).
- Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
- Evaluate the model’s performance by doing the following:
  - Calculate the accuracy score of the model.
  - Generate a confusion matrix.
  - Print the classification report.

Predict a Logistic Regression Model with Resampled Training Data


## Results

Describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

Precision: Ability of the models to predict false positives. Number of correct positives predictions over all predicted. 

Recall: Ability of the model to predict all positves and avoid negatives. Number of correct positives predictions over actual positives. 

Balanced Accuracy: Weighted avg of accuracy. Takes both precision and recall to show wich model is more correct with also weighted between both healhty and risky loans. 

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
    - The logistic regression model predicts both the '0' (healthy loan) and '1' (high-risk loan) realloy well. Healthy loans has 100% accuracy and f1-score and 99% in recall. High risk loans are less accurate with 85% accuracy and 91% recall. There are also more false negatives found with high risk loans than healthy loans. 

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
    - The second model performs just as well as the first model. We do see an uptick in high risk loans with the new model. Recall has increased from .91 to .99 which has overall increased the balanced accuracy score.


## Summary

* Summarize the results of the machine learning models:
  Overall, both models were both very accurate. Both performed almost 100% when it came to the healthy loans. When predicting high risk loans. Model 2 performed better showing more accurate results verified by the balanced accuracy score. Model 1 had a weighted balanced accuracy score of 95%. Model 2 had a balanced accuracy score of 99%. This was due to the increase in predicting accuracy in precision and recall for high risk loans. 