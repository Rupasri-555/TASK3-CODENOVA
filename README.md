# CreditGuard AI — Credit Card Default Prediction

## Project Summary
CreditGuard AI is a machine-learning project that predicts whether a credit-card customer is likely to default on their next payment. It also includes a separate rule-based bill-affordability check.

## Problem Statement
Credit-card default can create financial losses for lenders. This project explores historical customer data to predict default risk using machine-learning classification models.

## Dataset and Data Source
- Dataset: Default of Credit Card Clients
- Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)
- Records: 30,000
- Target: Default payment next month

## Exploratory Data Analysis
The notebook explores default distribution, customer characteristics, repayment status, bill amounts, payment amounts and feature correlations. Add the actual generated visualizations to the `outputs/` folder.

## Data Preprocessing
The project checks missing values and duplicates, cleans selected categorical codes, and uses imputation, categorical encoding and scaling where appropriate.

## Feature Engineering
Engineered features include average bill amount, average payment amount, delayed-payment count and average bill-to-credit-limit ratio.

## Models
The project compares a baseline classifier, Logistic Regression and Random Forest. Cross-validation and hyperparameter tuning are used where implemented in the notebook.

## Evaluation
Metrics include precision, recall, F1-score and ROC-AUC, with a confusion matrix and ROC curve.

Fill in the measured results from your notebook:
- Baseline F1-score: [Add actual result]
- Logistic Regression F1-score: [Add actual result]
- Random Forest F1-score: [Add actual result]
- Final model ROC-AUC: [Add actual result]

## Prediction Demo
The current simplified prediction model uses credit limit, bill amount and payment-delay status. Bank balance is used separately for the affordability calculation.

The custom credit-limit-versus-bank-balance rule is a project-specific rule, not a standard banking rule. The original dataset does not contain current bank balance, so the affordability check is not a trained machine-learning prediction.

## Limitations
- Predictions are estimates, not guarantees.
- The data is historical and may not represent current customers.
- Current bank balance and a direct affordability label are absent from the original dataset.
- The simplified three-feature model should be evaluated separately from the full-feature model.

## Technologies
Python, pandas, NumPy, scikit-learn, Matplotlib, Seaborn, joblib and Jupyter Notebook.

## How to Run
1. Install the packages listed in `requirements.txt`.
2. Download the dataset from the linked UCI source and place it in the expected data folder.
3. Open `notebooks/CreditGuard_AI_Task3.ipynb` in Jupyter Notebook.
4. Run the cells in order and review the evaluation results.

## Project Structure
```text
CreditGuard-AI/
├── data/
├── notebooks/
│   └── CreditGuard_AI_Task3.ipynb
├── models/
│   └── creditguard_model.joblib
├── outputs/
├── README.md
└── requirements.txt
```
