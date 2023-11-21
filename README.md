# credit-risk-classification

The credit_risk file contains the Jupyter Notebook, and the resources file contains the CSV file used for this analysis.

## Analysis
This analysis uses machine learning to aid in categorizing loans as healthy or high-risk.

The data consists of 75,036 healthy loans and 2,500 high-risk loans. This data was used to train the model.

X-values included the loan size, interest rate, borrower's income, debt-to-income ratio, number of accounts, number of derogatory marks, and total debt. The y-variable was loan status, which was classified by a 0 (healthy) or 1 (high-risk).

For this analysis, the x and y values were seperated and data was split into train and tests groups with a random state of 1. A logistic regression model was used, and predictions were made based on that model. A balanced accuracy score, confusion matrix and classification report were created to check the accuracy of the model.

The process was repeated on resampled data to create a more balanced data set of 56,271 healthy loans and the same number of high-risk loans. 

## Results
**Model One (Original Data)**
* Balanced Accuracy - 0.95
* Accuracy - 0.99
* Precision - 1.00 (healthy loans), 0.85 (high-risk loans)
* Recall - 0.99 (healthy loans), 0.91 (high-risk loans)

**Model Two (Resampled Data)**
* Balanced Accuracy - 0.99
* Accuracy - 0.99
* Precision - 1.00 (healthy loans), 0.84 (high-risk loans)
* Recall - 0.99 (healthy loans), 0.99 (high-risk loans)


## Summary
Both models are very accurate in predicting healthy loans, and not as accurate in the prediction of high-risk loans, which can create false positives (classifying a high-risk loan as healthy). This is due to fewer data points for high-risk loans (75,036 healthy loan data points vs 2500 high-risk loan data points).

The resampled data in the second model isn't overwhelmingly better, but still superior as it finds more instances of high-risk loans than the first model (16% vs 15 %), which is of great importance to a lender. 
