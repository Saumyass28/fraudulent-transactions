
# Fraud Detection Project

## Overview

This project involves developing a fraud detection system using machine learning techniques to identify fraudulent transactions. The goal is to enhance the accuracy and efficiency of detecting fraudulent activities within a financial dataset.

## Data Description

The dataset includes the following columns:
- `type`: Transaction type (e.g., PAYMENT, CASH_IN, etc.)
- `amount`: Transaction amount
- `oldbalanceOrg`: Original balance before the transaction
- `newbalanceOrig`: New balance after the transaction
- `oldbalanceDest`: Destination account’s balance before the transaction
- `newbalanceDest`: Destination account’s balance after the transaction
- `isFraud`: Indicator of whether the transaction is fraudulent (1 for fraud, 0 for non-fraud)
- `isFlaggedFraud`: Indicator of whether the transaction has been flagged as fraud by the system

## Data Cleaning and Preprocessing

1. **Handling Missing Values:** Imputation or removal of missing values as needed.
2. **Outliers:** Detection and treatment of outliers using statistical methods (e.g., IQR).
3. **Multi-Collinearity:** Identified and addressed using VIF to remove highly correlated features.

## Model Description

### Model Selection

- **Model Used:** XGBoost (eXtreme Gradient Boosting)
- **Features:** Selected based on feature importance and Recursive Feature Elimination (RFE).

### Training and Evaluation

- **Metrics:** Precision, Recall, AUC, and Confusion Matrix are used for evaluating model performance.
- **Tools:** Visualizations include ROC curves and feature importance plots.

## Key Factors for Fraud Detection

- **Important Predictors:** Transaction amount, changes in account balances, and flagged transactions.
- **Rationale:** Higher transaction amounts and significant balance changes are strong indicators of potential fraud.

## Prevention Measures

- **Infrastructure Updates:** Implement real-time monitoring and anomaly detection systems to prevent fraudulent transactions.

## Evaluation of Measures

- **Assessment:** Monitor changes in fraud detection rates and model performance metrics to determine the effectiveness of implemented measures.

## Requirements

- Python 3.x
- Required libraries: pandas, numpy, scikit-learn, xgboost, matplotlib, seaborn

## Installation

To install the necessary libraries, use the following command:

```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn
```

## Usage

1. **Data Loading:** Load the dataset into a pandas DataFrame.
2. **Preprocessing:** Perform data cleaning and feature selection.
3. **Model Training:** Train the XGBoost model on the preprocessed data.
4. **Evaluation:** Evaluate model performance and visualize results.
5. **Deployment:** Implement the model into a real-time fraud detection system.

