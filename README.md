# Loan Credit Risk 

This project implements and compares multiple machine learning algorithms to predict loan approval outcomes (Class 0: Rejected, Class 1: Approved) based on applicant credit risk profiles.

## 📊 Model Performance Summary

We evaluated three different classifiers to balance financial risk management against business revenue goals:

### 1. Baseline Model (Logistic Regression)
* **Test Accuracy:** ~80%
* **Characteristics:** Provided a solid baseline with balanced recall, but left room for optimization in reducing false positives and false negatives.

### 2. Random Forest Classifier (`Rfc`)
* **Test Accuracy:** ~95%
* **Class 1 Precision:** 1.00 (100%)
* **False Positives:** Only 3 
* **Best For:** **Extreme Risk Aversion**. With near-zero false positives, this model virtually eliminates the risk of approving a toxic loan that might result in a default.

### 3. XGBoost Classifier (`Xgb`)
* **Test Accuracy:** ~97%
* **False Negatives:** 14 (Down from 62)
* **Best For:** **Revenue Maximization**. By significantly reducing false negatives, this model recovers missed revenue by successfully approving 48 more qualified applicants than the Random Forest model.

## 🛠️ Tech Stack
* **Environment:** Jupyter Notebook / JupyterLab
* **Libraries:** Python, Scikit-Learn, XGBoost, Pandas, NumPy
*
