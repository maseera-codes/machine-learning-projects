# Bank Marketing Subscription Prediction

## Project Overview

This project uses machine learning classification techniques to predict whether a bank customer will subscribe to a term deposit.

The project uses the Bank Marketing dataset and follows an end-to-end machine learning workflow, including data exploration, preprocessing, model training, evaluation, and model comparison.

## Objective

The main objective is to predict the target variable `y`:

- `yes` → Customer subscribed to a term deposit
- `no` → Customer did not subscribe

## Dataset

The dataset contains 45,211 customer records and 17 columns.

### Main Features

- Age
- Job
- Marital Status
- Education
- Default
- Balance
- Housing Loan
- Personal Loan
- Contact
- Day
- Month
- Campaign
- Pdays
- Previous
- Poutcome

### Target

`y` — Term deposit subscription

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Machine Learning Models

The following classification algorithms were evaluated:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Gradient Boosting

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- ROC-AUC

## Model Comparison

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 90.10% | 63.98% | 35.26% | 45.46% |
| Decision Tree | 90.11% | 68.82% | 43.57% | 50.77% |
| Random Forest (with duration) | 84.50% | 41.96% | 85.11% | 56.24% |
| Gradient Boosting | 90.55% | 65.26% | 41.02% | 50.38% |
| Random Forest (without duration) | 81.65% | 33.94% | 60.02% | 43.36% |

## Important Feature Consideration

The `duration` feature represents the length of the marketing call.

Because call duration may only be known during or after a customer interaction, a separate Random Forest model was evaluated without this feature to examine a more realistic pre-call prediction scenario.

## Key Findings

- The dataset has a strong class imbalance, with considerably more customers who did not subscribe.
- Accuracy alone does not fully describe classification performance on this imbalanced dataset.
- Random Forest with `duration` achieved the highest recall and F1 score among the tested models.
- Removing `duration` changed model performance considerably.
- The experiment demonstrates the importance of considering feature availability and multiple evaluation metrics.

## Project Workflow

1. Data Loading
2. Data Understanding
3. Data Quality Checks
4. Exploratory Data Analysis
5. Target Variable Analysis
6. Feature Preparation
7. Train-Test Split
8. Categorical Encoding
9. Model Training
10. Model Evaluation
11. Feature Importance Analysis
12. Model Comparison
13. Final Conclusions

## Project Files

- `Classification-project.ipynb` — Complete analysis and machine learning implementation
- `README.md` — Project documentation

## Conclusion

This project demonstrates an end-to-end machine learning classification workflow for predicting bank term-deposit subscriptions. It also shows how class imbalance, evaluation metrics, and feature availability can affect model performance.
