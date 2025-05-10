# ❤️ Heart Disease Prediction using Machine Learning

This project aims to predict the presence of heart disease in patients using a machine learning approach. It leverages health-related features such as age, cholesterol levels, and chest pain type, applying a **Logistic Regression** classifier to make accurate predictions.

## 📌 Project Overview

Heart disease is a leading cause of mortality globally. Early detection through machine learning can enable timely medical intervention and save lives. This project uses the UCI Heart Disease dataset to build a supervised learning model.

---

## 🚀 Features

- Predicts whether a patient has heart disease (binary classification)
- Uses Logistic Regression for simplicity and effectiveness
- Accepts input for 13 medical attributes
- Easy-to-understand prediction output (Heart Disease / No Heart Disease)
- Suitable as a base for a medical diagnostic tool

---

## 📂 Dataset

- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Heart+Disease)
- **Instances:** 303
- **Features:** 13
  - Age, Sex, Chest Pain Type, Resting Blood Pressure, Cholesterol, Fasting Blood Sugar, etc.
- **Target:** `1` (has heart disease), `0` (no heart disease)

---

## 🛠️ Tech Stack

- Python 3.x
- Jupyter Notebook
- Libraries:
  - NumPy
  - Pandas
  - Scikit-learn (Logistic Regression, train-test split, accuracy)

---

## 🧠 Model Training & Evaluation

- Logistic Regression trained on 80% of the data
- Tested on 20% of the data
- **Accuracy:**
  - Training: ~85.2%
  - Testing: ~81.9%

---

## 🧪 Sample Prediction

```python
input_data = (41, 0, 1, 130, 204, 0, 0, 172, 0, 1.4, 2, 0, 2)
# Output: The person is suffering from Heart Disease
