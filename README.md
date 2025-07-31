# Breast Cancer Survival Prediction Using Decision Tree Regression

This project focuses on predicting **breast cancer patient survival duration (in months)** using supervised machine learning. Specifically, two **Decision Tree Regression** models are built and evaluated to help healthcare professionals identify patients at higher risk and prioritize treatments accordingly.

---

## 📚 Project Overview

This analysis follows a structured machine learning pipeline and is aligned with healthcare modeling objectives.

### Objectives:
- Predict **Survival_Months** using clinical and demographic patient data.
- Compare two regression models:
  - **DT-1**: Fully grown Decision Tree
  - **DT-2**: Pruned Decision Tree with a maximum depth of 4
- Evaluate models using performance metrics relevant to clinical risk minimization.

---

## 📊 Dataset

- **File**: `survival_df.csv`
- **Target Variable**: `Survival_Months`
- **Features Used** (example):
  - Age, Tumor Stage, Tumor Size
  - Hormone Receptor Status (Estrogen, Progesterone)
  - Regional Node Status
  - Grade, Differentiation, etc.

---

## ⚙️ Models & Techniques

### 🔹 Preprocessing
- Features and target separated
- Train/Test split: 60/40 using `train_test_split()`

### 🔹 Regression Models
1. **DT-1**: Fully grown Decision Tree
   ```python
   from sklearn.tree import DecisionTreeRegressor
   DT_1 = DecisionTreeRegressor()
   DT_1.fit(X_train, y_train)
   y1_pred = DT_1.predict(X_test)
