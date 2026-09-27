# Medical Insurance Cost Prediction

## Project Overview

This project uses machine learning regression techniques to predict medical insurance charges based on demographic and health-related information.

The project follows an end-to-end machine learning workflow including data exploration, preprocessing, model training, evaluation, hyperparameter tuning, and prediction.

## Objective

The main objective is to predict the medical insurance cost (`charges`) for an individual based on features such as age, BMI, smoking status, and other demographic factors.

## Dataset

The dataset contains 1,338 records and 7 columns.

### Features

- Age
- Sex
- BMI
- Children
- Smoker
- Region

### Target

`charges` — Medical insurance cost

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Machine Learning Models

The following regression models were evaluated:

1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. Decision Tree Regressor
5. Random Forest Regressor
6. Gradient Boosting Regressor

Gradient Boosting was further tuned using GridSearchCV.

## Model Evaluation

The models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

### Model Comparison

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 4181.19 | 5796.28 | 0.7836 |
| Ridge Regression | 4182.80 | 5796.98 | 0.7835 |
| Lasso Regression | 4181.51 | 5796.65 | 0.7836 |
| Decision Tree | 2930.77 | 5082.51 | 0.8336 |
| Random Forest | 2559.90 | 4586.94 | 0.8645 |
| Gradient Boosting | 2457.57 | 4310.09 | 0.8803 |
| Tuned Gradient Boosting | 2410.63 | 4309.10 | 0.8804 |

## Hyperparameter Tuning

GridSearchCV was used to tune the Gradient Boosting model.

Best parameters:

- `learning_rate = 0.05`
- `max_depth = 2`
- `n_estimators = 300`

## Key Findings

- Smoking status was the most influential feature in predicting insurance charges.
- BMI and age also had an important relationship with insurance costs.
- Tree-based ensemble models performed better than the linear regression models tested.
- The tuned Gradient Boosting model achieved an R² score of approximately 0.88 on the test set.

## Example Prediction

An example prediction was generated for a 35-year-old female with:

- BMI: 28
- Children: 0
- Smoker: No
- Region: Southwest

The predicted insurance charge was approximately **$6,167.67**.

## Project Workflow

1. Data Loading
2. Data Understanding
3. Data Quality Checks
4. Exploratory Data Analysis
5. Feature and Target Selection
6. Train-Test Split
7. Data Preprocessing
8. Model Training
9. Model Evaluation
10. Hyperparameter Tuning
11. Feature Importance Analysis
12. Example Prediction
13. Final Conclusion

## Project Files

- `medical_insurance_cost_prediction.ipynb` — Complete analysis and machine learning implementation
- `README.md` — Project documentation

## Conclusion

This project demonstrates an end-to-end machine learning regression workflow for predicting medical insurance costs. It also demonstrates the use of preprocessing pipelines, multiple regression algorithms, model evaluation, and hyperparameter tuning.
