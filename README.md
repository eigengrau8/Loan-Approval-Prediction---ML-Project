# 🏦 Loan Approval Prediction - ML Project

## 📌 Objective

To develop a machine learning model that predicts whether a loan application will be approved based on applicant demographics and financial data. This project simulates real-world data issues and helps automate decisions in financial institutions.

---

## 📁 Dataset Overview

- **Size:** 100,000 rows × 13 columns
- **Target Variable:** Loan_Status (Y = approved, N = denied)

### 🔸 Features

| Type | Features |
|------|----------|
| Categorical | Gender, Married, Education, Self_Employed, Property_Area, Dependents |
| Numerical | ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History, Age |

---

## ⚙️ Workflow

1. **Data Cleaning**
   - Converted data types
   - Handled missing and negative values
   - Outlier treatment

2. **Feature Engineering**
   - Total income
   - EMI
   - Income-to-loan ratio
   - One-hot encoding

3. **Exploratory Data Analysis**
   - Univariate & bivariate plots
   - Correlation matrix
   - Multicollinearity check (VIF)

4. **Model Building**
   - Random Forest (primary)
   - Logistic Regression
   - XGBoost

5. **Evaluation**
   - Classification Report
   - Confusion Matrix
   - ROC AUC Score

---

## 📊 Results

- **Accuracy:** 77%
- **ROC AUC:** 0.78
- **Insights:**
  - EMI and Credit Score most predictive
  - Recall for approved loans is very high (0.97)
  - Model performs well but leans towards approving loans

---

## 🧠 Key Learnings

- End-to-end pipeline: cleaning → EDA → modeling
- Realistic feature engineering and handling messy data
- Understanding trade-off between precision and recall in financial applications
- Addressing class imbalance without oversampling

---

