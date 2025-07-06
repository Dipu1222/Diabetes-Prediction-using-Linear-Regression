# Diabetes Prediction using Linear Regression

This project demonstrates how to predict the presence of diabetes using a Linear Regression model trained on a diabetes dataset. The project involves preprocessing data, training a model, and evaluating its performance.

---

## Dataset

The dataset used in this project is a diabetes dataset stored in `diabetes.csv`. It contains medical predictor variables and one target variable indicating whether a patient has diabetes (`1`) or not (`0`).

The key features include:
- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

---

## Data Preprocessing

- Zero values in columns that should not be zero (Glucose, BloodPressure, SkinThickness, Insulin, BMI) are replaced with the median of non-zero values in the respective column.
- Special adjustment: The first row's `Glucose` value is replaced with the maximum `Glucose` value, and for records with the lowest `Age`, the `Glucose` value is replaced with the minimum `Glucose`.

---

## Model

- The project uses **Linear Regression** to predict the diabetes outcome.
- The dataset is split into training and testing sets (80% train, 20% test).
- The continuous output from the Linear Regression model is rounded to the nearest integer to get discrete class predictions (0 or 1).

---

## Evaluation Metrics

The model is evaluated using the following metrics:
- Accuracy
- Confusion Matrix
- Precision
- Recall
- F1 Score

---

## How to Run

1. Clone this repository.
2. Make sure you have Python installed along with the necessary libraries:
   ```bash
   pip install pandas numpy scikit-learn
