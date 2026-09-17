# 🫀 Heart Disease Prediction Model

> Machine Learning classification model predicting cardiovascular disease risk based on clinical patient health metrics using Python and Scikit-Learn.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-ML-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

---

## ⭐ Star Schema (Clinical Data Warehouse Model)

```
                            +-----------------------------------+
                            |           Dim_Patient             |
                            +-----------------------------------+
                            | Patient_Key (PK)                  |
                            | Age                               |
                            | Sex (Male/Female)                 |
                            | MedicalHistory                    |
                            +-----------------+-----------------+
                                              | 1
                                              |
                                              | N
+-----------------------+   +-----------------+-----------------+   +-----------------------+
|  Dim_Calendar         | 1 |      Fact_PatientDiagnosis        | 1 |  Dim_ClinicalTest     |
+-----------------------+---+-----------------------------------+---+-----------------------+
| Date_Key (PK)         | N | Diagnosis_Key (PK)                | N | Test_Key (PK)         |
| Full_Date             |   | Date_Key (FK)                     |   | Test_Name             |
| Month / Year          |   | Patient_Key (FK)                  |   | Normal_Range          |
+-----------------------+   | Test_Key (FK)                     |   +-----------------------+
                            | Trestbps_mmHg (Measure)           |
                            | Serum_Cholesterol_mgdl (Measure)  |
                            | Max_HeartRate_Thalach (Measure)   |
                            | ST_Depression_Oldpeak (Measure)   |
                            | Target_HeartDisease (Measure)     |
                            +-----------------------------------+
```

---

## 📑 Clinical Input Feature Schema

| Attribute | Field Name | Data Type | Description & Valid Ranges |
| :--- | :--- | :--- | :--- |
| **Age** | `age` | Integer | Patient age in years ($29 - 77$) |
| **Sex** | `sex` | Categorical | $1 = \text{Male}, 0 = \text{Female}$ |
| **Chest Pain** | `cp` | Categorical | $0$: Typical, $1$: Atypical, $2$: Non-anginal, $3$: Asymptomatic |
| **Blood Pressure** | `trestbps` | Float | Resting blood pressure in mm Hg ($94 - 200$) |
| **Cholesterol** | `chol` | Float | Serum cholesterol in mg/dl ($126 - 564$) |
| **Target Output** | `target` | Binary | **$1 = \text{Heart Disease Risk Present}, 0 = \text{Healthy}$** |

---

## 🚀 Running the Notebook

```bash
git clone https://github.com/SamarthYete/Heart_Disease_Prediction_Model.git
cd Heart_Disease_Prediction_Model
pip install notebook pandas numpy scikit-learn seaborn matplotlib
jupyter notebook
```
