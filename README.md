# Hazardous Asteroids Detection

This project analyzes Near-Earth Object (NEO) data to detect potentially hazardous asteroids using three classification models:
- Logistic Regression
- Random Forest
- XGBoost

## Objective

The goal is to assess the effectiveness of various supervised machine learning methods in identifying asteroids that may pose a risk to Earth. The models focus on maximizing recall to reduce the chance of missing dangerous objects.

## Dataset

Source: [NASA NEO dataset](https://neo.ssa.esa.int/) (assumed origin – can be adjusted)

## Features Used

- Absolute magnitude
- Estimated minimum diameter
- Estimated maximum diameter
- Relative velocity
- Miss distance

## Models & Evaluation

Three models were trained and tested with class imbalance taken into account:
- **Logistic Regression**: good recall (93%) but low precision
- **Random Forest**: improved accuracy, limited gain in recall
- **XGBoost**: best recall (93%), but still low F1-score due to false positives

Visualizations include:
- Confusion matrix
- Top 10 most dangerous asteroids (by predicted probability)

## Technologies Used

- Python (pandas, scikit-learn, xgboost, seaborn, matplotlib)
- Jupyter Notebook

## Key Insights

- **Recall** is prioritized over precision in this case to ensure dangerous asteroids are not missed.
- XGBoost provided the most reliable detection rate for hazardous objects.
- Feature scaling and class weighting significantly impacted model performance.

## Final Output

Bar chart of the top 10 most hazardous asteroids with predicted probabilities (based on XGBoost model).

---

