# Customer Churn Prediction

A machine learning project that predicts whether a bank customer will churn (leave) based on their account and demographic details.

---

## About the Project

This project builds a binary classification model to identify customers likely to churn. Understanding churn patterns helps businesses take proactive retention measures. A Decision Tree classifier was used, and feature importance was analyzed to understand which factors drive customer churn the most.

---

## Dataset

- **File:** `customer_churn_data.csv`
- **Records:** 10,000 customers
- **Features Used:**
  - CreditScore, Geography, Gender, Age, Tenure
  - Balance, NumOfProducts, HasCrCard
  - IsActiveMember, EstimatedSalary
- **Dropped Columns:** RowNumber, CustomerId, Surname (irrelevant to prediction)
- **Target:** `Exited` (1 = Churned, 0 = Retained)

---

## Workflow

1. Loaded and explored the dataset
2. Performed EDA — customer churn distribution
3. Dropped irrelevant columns (RowNumber, CustomerId, Surname)
4. Label encoded categorical columns (Geography, Gender)
5. Split data into 80% train and 20% test
6. Trained a Decision Tree classifier
7. Evaluated using Accuracy, Confusion Matrix, and Classification Report
8. Plotted Feature Importance to identify key churn drivers

---

## Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

## Results

### Decision Tree
| Metric | Value |
|--------|-------|
| Accuracy | 78.2% |
| Precision (Churned) | 0.45 |
| Recall (Churned) | 0.52 |
| F1-Score (Churned) | 0.49 |

> **Note:** The dataset is imbalanced — 8093 retained vs 1907 churned customers. The model performs well on the majority class (Retained — Recall: 85%) but struggles on the minority class (Churned — Recall: 52%). Techniques like SMOTE or class_weight balancing could improve churn detection in future iterations.

---

## Files

| File | Description |
|------|-------------|
| `customer_churn_code.ipynb` | Main notebook — EDA, model training, feature importance, evaluation |
| `customer_churn_data.csv` | Dataset |

---

*Developed by Prince Joshi | Aspiring Data Analyst*
