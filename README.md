# Customer Churn Classification

## Problem statement

Telecom companies want to know which customers may leave their service. This project uses customer information to predict whether a customer will **stay** or **churn**.

## What we did

1. Downloaded and cleaned the Telco Customer Churn data.
2. Explored churn rates and checked correlations between numeric features.
3. Prepared the data for machine learning by converting text answers into numbers and filling missing values.
4. Trained and compared three Scikit-learn classification models: logistic regression, random forest, and gradient boosting.
5. Compared the models using F1 score and reviewed the best model with a confusion matrix and classification report.

## Result

Gradient boosting had the highest F1 score in the current run: **0.637** on the test data. The model predicts churn (`1`) or staying (`0`). This helps identify customers who may be at risk of leaving; it does not guarantee what a customer will do.

## How the model predicts

The model learns patterns from customer details such as tenure, contract type, and monthly charges. During training, it compares those details with each customer's known churn result. For a new customer record, it uses the learned patterns to predict one of two labels:

- `1` — the customer is predicted to churn.
- `0` — the customer is predicted to stay.

## Conclusion

This project shows that customer information can be used to identify customers who may leave. Gradient boosting performed best among the three models in the current run. The result can help a telecom company decide which customers to review for possible support or retention offers. The prediction is an estimate, not a certainty.

## Run the notebooks

Run these notebooks in order:

1. `Notebooks/01_data_cleaning.ipynb`
2. `Notebooks/02_eda_feature_engineering.ipynb`
3. `Notebooks/03_model_building.ipynb`

Install the required packages with:

```bash
pip install -r requirements.txt
```
# Week_2_Target_Customer_Churn_Prediction_using_classification
