# Credit Risk Classification

## Overview
The purpose of this analysis is to build a machine learning model that can accurately identify the creditworthiness of borrowers using historical lending data from a peer-to-peer lending service company. This analysis aims to help the company assess the risk of default on loans by predicting whether a loan is healthy or high-risk.

## Analysis
### Purpose of the Analysis
The goal of this analysis is to predict the credit risk associated with loans using logistic regression. By doing so, the company can better manage lending decisions and minimize potential losses from high-risk loans.

### Data Description
The dataset contains financial information on historical lending activities. Key variables include:
- **Loan Status (`loan_status`)**: The target variable indicating if a loan is healthy (0) or high-risk (1).
- **Financial Features**: Various financial metrics used as predictors, such as annual income, debt-to-income ratio, number of open accounts, credit score, etc.

### Variable Information
- **Target Variable (`loan_status`)**:
  - 0: Healthy loan
  - 1: High-risk loan
- **Feature Variables**: Annual income, debt-to-income ratio, credit score, etc.

### Stages of the Machine Learning Process
1. **Data Preparation**:
   - Loaded the dataset and created labels (`y`) from the `loan_status` column.
   - Created the feature set (`X`) from the remaining columns.
   - Split the data into training and testing sets using `train_test_split`.

2. **Model Building**:
   - Used logistic regression (`LogisticRegression`) to build the model.
   - Trained the model using the training data.

3. **Model Evaluation**:
   - Generated predictions using the testing data.
   - Evaluated the model performance using confusion matrix and classification report to calculate precision, recall, and accuracy.

### Methods Used
- **Logistic Regression (`LogisticRegression`)**:
  - Chosen for its simplicity and effectiveness in binary classification problems.

## Results
### Machine Learning Model 1: Logistic Regression
- **Accuracy**: 0.99
- **Precision for Healthy Loans (0)**: 1.00
- **Recall for Healthy Loans (0)**: 0.99
- **Precision for High-Risk Loans (1)**: 0.85
- **Recall for High-Risk Loans (1)**: 0.91

## Summary
The logistic regression model demonstrated excellent performance in predicting both healthy and high-risk loans.

- **Healthy Loans (label 0)**:
  - **Precision**: 1.00 - All loans predicted as healthy were actually healthy.
  - **Recall**: 0.99 - Nearly all healthy loans were correctly identified.
  
- **High-Risk Loans (label 1)**:
  - **Precision**: 0.85 - 85% of loans predicted as high-risk were actually high-risk.
  - **Recall**: 0.91 - 91% of actual high-risk loans were correctly identified.

### Recommendation
The logistic regression model performs exceptionally well in predicting loan statuses with a high accuracy of 0.99. It effectively identifies both healthy and high-risk loans, which is crucial for making informed lending decisions. Given these results, I recommend using this logistic regression model to assist in the loan approval process. Its high precision and recall scores for both labels indicate that it is a reliable and effective tool for credit risk assessment. However, further tuning and continuous validation are suggested to maintain and improve the model's performance over time.
