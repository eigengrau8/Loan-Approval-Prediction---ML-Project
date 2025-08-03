# Loan-Approval-Prediction---ML-Project
A machine learning project to predict whether a loan application will be approved, based on applicant financial and personal information.

## 📂 Dataset
- Total records: 10,000 (sampled from larger dataset)
- Features include income, credit history, dependents, loan amount, and more.

## 🔍 Objective
Build a classification model to predict `Loan_Status` (Approved/Not Approved).

## 🧹 Data Preprocessing
- Handled missing values using mean/median for numerical and mode for categorical features.
- Feature engineering:
  - `TotalIncome` = `ApplicantIncome` + `CoapplicantIncome`
  - `EMI` = `LoanAmount` / `Loan_Amount_Term`
  - `Balance_Income` = `TotalIncome` – `EMI`
- One-Hot Encoding for categorical variables.
- Addressed outliers using IQR-based filtering and log transformation where needed.
- Scaled numerical features where appropriate.

## 🧠 Modeling
- Used `RandomForestClassifier` from scikit-learn.
- Stratified train-test split to handle class imbalance.
- 5-fold cross-validation used for robust evaluation.

## 📊 Evaluation
- Average F1 Score: **~0.80**
- High recall on approved loans; good precision on both classes.
- Feature importance showed that income-related features were key predictors.

## 🔍 Key Findings
- **Top predictors**: CoapplicantIncome, ApplicantIncome, TotalIncome, Balance_Income.
- Applicants with higher disposable income (post-EMI) were more likely to be approved.
- Credit history played a supporting role in approval decisions.

## 📁 Project Files
- `loan_approval_prediction.ipynb`: Full notebook with preprocessing, EDA, modeling, and evaluation.
- `loan_data.csv`: Cleaned dataset used for model training.
