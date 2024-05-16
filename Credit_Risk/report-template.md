# Module 20 Credit Risk Classification Report

## Purpose
This project aims to test the usefulness of a logistic regression model for identifying healthy and high-risk loans. Historical data of lending activity from peer-to-peer lending services was provided to train and test the model in efforts to identify the creditworthiness of borrowers.

## Data
The historical lending data used to train the model included 77,536 examples. The features used to predict the creditworthiness of the borrower included basic information about the loan and the borrower's current financial health.

Fields provided in the data are detailed below:
* `loan_size`: Loan amount in dollars
* `interest_rate`: Interest rate for the provided loan
* `borrower_income`: Annual income of the borrower
* `debt_to_income`: Debt-to-income ratio
* `num_of_accounts`: Number of accounts the borrower holds
* `derogatory_marks`: Number of derogatory marks against the borrower
* `total_debt`: Total debt of the borrower
* `loan_status`: 0 identifies a "Healthy loan" and 1 identifies a "High-risk loan"

## Modeling Stages
1. Data was imported into Pandas and the features set (X) was split from the labels (y) set. The label in this model is `loan_status`, and the features include all other columns.
2. Data was split into a 75/25 train/test ratio.
3. A Logistic Regression model from the scikit-learn library was utilized.
4. The model was fit with the training data.
5. Predictions were generated using the features test data and compared against the actual results from the label data.
6. Confusion Matrix and Classification Reports were generated to evaluate the model.

## Results

### Classification Report
* **Healthy Loan**
    * `Precision`: 1.00
    * `Recall`: 1.00
    * `F1-Score`: 1.00

* **High-risk Loan**
    * `Precision`: 0.87
    * `Recall`: 0.95
    * `F1-Score`: 0.91

* **Overall Model**
    * `Accuracy`: 0.99

## Summary

Based on the confusion matrix and the classification report, the Logistic Regression model performs exceptionally well in predicting healthy loan statuses. This is evidenced by precision, recall, and F1-scores all being 1. However, the model did not perform as well for high-risk loan prediction. The precision score of 0.87 indicates a slight issue with false positives, where some healthy loans were identified as high-risk. The recall for high-risk loans is high at 0.95, meaning the model successfully identifies most high-risk loans. The high accuracy, macro average, and weighted average scores demonstrate that the model is strong overall, but there is still a need to improve in reducing the misclassification of healthy loans as high-risk.

