# loan-approval-analysis
# Loan Approval Analysis (Logistic Regression)

This project analyzes loan applicant data to understand the factors that influence loan approval decisions.  
The goal is to identify which applicant characteristics most strongly affect approval likelihood and to build an interpretable model that aligns with banking risk evaluation practices.

---

## Problem Statement
Banks must balance two risks:
1. Approving loans for applicants who may default.
2. Rejecting reliable applicants, losing business.

This project examines applicant data to determine the strongest predictors of loan approval and builds a transparent model for decision support.

---

## Dataset
Source: Kaggle – Loan Prediction Dataset  
(Download Link: https://www.kaggle.com/datasets/ninzaami/loan-predication)

Target Variable:
- **Loan_Status** (1 = Approved, 0 = Not Approved)

Key Features Used:
- ApplicantIncome
- CoapplicantIncome
- LoanAmount
- Credit_History
- Education
- Gender
- Married

---

## Approach

### 1. Data Cleaning
- Imputed missing values using median (numerical) and mode (categorical)
- Encoded categorical variables using `LabelEncoder`

### 2. Exploratory Data Analysis (EDA)
Key insights:
- **Credit History is the dominant factor** in loan approval decisions.
- Applicants with Credit_History = 1 had ~4x higher approval likelihood.
- Income influences approval probability only after repayment reliability is established.
- Education and gender show weaker secondary effects.

### 3. Model
A **Logistic Regression** model was chosen for interpretability, aligning with financial decision transparency requirements.

Evaluation Metrics:
- Accuracy
- Confusion Matrix
- Classification Report (Precision, Recall, F1 Score)

---

## Results

| Factor | Influence on Approval |
|-------|------------------------|
| **Credit History** | Strongest predictor (primary signal) |
| Applicant Income | Secondary influence |
| Education | Minor influence |
| Marital Status | Minimal effect |

**Conclusion:**  
Loan approval is **trust-driven**, not income-driven.  
Applicants with proven repayment history are significantly more likely to be approved.

---

## Why Logistic Regression?
- Transparent and explainable
- Coefficients provide clear feature impact direction
- Banks require interpretability due to regulatory & compliance constraints

---

## Tools Used
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-Learn
- Google Colab

---

## Author
**Shubham Kumar**  
B.Tech Mechanical Engineering, DTU  
Email: shubhamkumar_23me255@dtu.ac.in  
