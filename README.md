# 💳 Credit Risk Prediction Model

A machine learning project focused on predicting loan defaults in the fintech sector. This project emphasizes scientific defensibility, rigorous data cleaning, and the elimination of Data Leakage to build a realistic and production-ready predictive model.

---

## 🚀 Project Overview
In retail banking and lending, predicting whether a borrower will default on a loan is critical for risk management. This project builds a Random Forest Classifier to evaluate credit risk based on customer attributes while carefully avoiding artificial performance inflation.

---

## 🛠️ Key Challenges & Data Cleaning (Handling Data Leakage)
During the initial exploratory data analysis, the model achieved a 100% accuracy score (ROC-AUC = 1.0). Further investigation revealed Data Leakage caused by target-dependent and post-origination variables (such as default_date, loss_given_default, and collection metrics) that leaked the future outcome to the model.

Actions Taken:
* Removed post-default and leakage-prone columns to ensure the model only relies on information available *at the time of loan application*.
* Handled categorical variables using LabelEncoder.
* Standardized features and split data into training and test sets (80/20 split with stratification).

---

## 📈 Model Performance
After removing data leakage and validating the model on unseen test data, the pipeline achieved a reliable and robust performance:
* ROC-AUC Score: ~0.75 (A realistic, defensible, and generalizable performance metric reflecting true real-world efficacy).
* Evaluation Metrics: Evaluated using Precision, Recall, F1-Score, and ROC curves to manage class imbalance effectively.

---

## 📊 Features Used
The model evaluates applicants based on core pre-origination attributes:
* credit_score (Borrower credit score)
* initial_rating (Initial risk rating)
* leverage & interest_coverage (Financial pressure indicators)
* ead (Exposure at Default)
* coupon_rate & maturity_months

---

## ⚙️ Tech Stack & Libraries
* Python
* Pandas & NumPy (Data Manipulation)
* Scikit-Learn (Random Forest Classifier, Evaluation Metrics, Preprocessing)
* Matplotlib (Data Visualization & ROC Curves)

---

## 📦 How to Run
1. Clone the repository:
   `bash
   git clone [https://github.com/your-username/Credit-Risk-Prediction-Model.git](https://github.com/your-username/Credit-Risk-Prediction-Model.git)
