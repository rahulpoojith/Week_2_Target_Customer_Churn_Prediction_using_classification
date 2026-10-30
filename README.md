# Week 2: Customer Churn Prediction Using Classification

## Problem statement

Telecom companies want to identify customers who may leave their service. This project uses customer information to predict whether a customer will stay or churn.

## What we did

1. Downloaded and cleaned the Telco Customer Churn data.
2. Explored churn rates and checked correlations between numeric features.
3. Converted text answers into numeric columns and filled missing values.
4. Trained and compared logistic regression, random forest, and gradient boosting classifiers.
5. Evaluated the models using F1 score, a confusion matrix, and a classification report.

## What the model predicts

The model uses details such as a customer's tenure, contract, and charges to predict one of two labels:

- `1`: the customer is predicted to churn.
- `0`: the customer is predicted to stay.

It predicts a class label; it does not explain why a customer might leave or guarantee what they will do.

## Results and conclusion

Gradient boosting had the highest F1 score among the three models in the current run: **0.637**. On the 1,409 customer test set, it had **76% accuracy**, **53% precision** for churn, and **79% recall** for churn.

The confusion matrix was:

| Actual outcome | Predicted stayed | Predicted churned |
| --- | ---: | ---: |
| Stayed | 773 | 262 |
| Churned | 77 | 297 |

The model found 297 of the 374 customers who churned and missed 77. It also flagged 262 customers who stayed as likely to churn. This means it can help a company create a list of customers to review, but that list will include false alarms. It should support retention work rather than make decisions on its own.

These results come from one train/test split, and the same test set was used to compare the three models. The scores are a useful project result, not a guarantee of performance on future customers.

## Run the notebooks

Run these notebooks in order:

1. `Notebooks/01_data_cleaning.ipynb`
2. `Notebooks/02_eda_feature_engineering.ipynb`
3. `Notebooks/03_model_building.ipynb`

Install the required packages with:

```bash
pip install -r requirements.txt
```
