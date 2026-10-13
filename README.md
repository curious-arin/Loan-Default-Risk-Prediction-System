# Loan Default Risk Prediction System 💵

## 🙂 Overview

This project focuses on predicting loan default risk for banking and financial services. By analyzing borrower demographic, financial, employment, credit history, and loan characteristics, i have built a machine learning classification model to identify high-risk borrowers before loan approval.

*The goal is to support safer, data-driven lending decisions, reduce financial losses, and strengthen credit risk management across lending operations.*

-----

## 💡 Problem Statement & Business Impact

- Financial institutions need reliable risk assessments before approving loans to prevent credit defaults.
- Unpredictable borrower defaults can lead to severe financial losses and inefficient credit operations.
- Default risk varies based on factors such as borrower income, debt-to-income ratio, employment stability, credit history, and loan purpose.
- Goal: Develop a classification model that predicts loan default risk (0 for No Default, 1 for Default) using information available during loan application review.
- Business value: Identifying high-risk borrowers early helps reduce credit losses, improves data-driven lending decisions, enhances automated and scalable risk assessment, and strengthens overall portfolio health.

-----

## 📂 Project Structure

Loan-Default-Risk-Prediction-System/
│
├── data/
│   └── Loan_default.csv
│
├── images/                                                 # EDA charts and visualizations
│
├── model/                                                  # Saved machine learning model
|   └── loan_default_risk_model.pkl                                                 
│
├── notebooks/                                              # Jupyter notebooks for analysis and modeling
│   ├── 1_Exploratory_Data_Analysis.ipynb
│   └── 2_Data_Preparation_and_Model_Training.ipynb
│
├── .gitignore            
├── app.py                                                  # Streamlit application
├── LICENSE
├── README.md
└── requirements.txt

-----

## 🔗 Dataset Source

[Loan Default Prediction Dataset](https://www.kaggle.com/datasets/nikhil1e9/loan-default)

The dataset contains borrower information such as income, employment details, credit history, loan characteristics, and repayment behavior. The target variable is Default (0 → No Default, 1 → Default).

-----

## 📊 Dataset Overview

- The dataset contains borrower and loan features used to classify default risk.
- Dataset features: Borrower demographic, financial, employment, credit, and loan-related information.
- Target variable: Default (0 = No Default, 1 = Defaulted).

-----

## 🚀 How to Run the Application Locally

Follow these steps to run the application on your local system.

### 1. Clone the Repository

```bash
git clone https://github.com/neuralarin/Loan-Default-Risk-Prediction-System.git

cd Loan-Default-Risk-Prediction-System
```

### 2. Create and Activate a Virtual Environment

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the virtual environment on **Windows PowerShell**:

```powershell
.\.venv\Scripts\Activate.ps1
```

-----

## 🔄 Workflow

### 1. Data Analysis

* Performed EDA to understand borrower behavior.
* Analyzed feature distributions and default patterns.

### 2. Feature Engineering

* Created important default indicating features like Loan_to_Income, Income_per_CreditLine, Employment_Stability and Interest_Burden
* Prepared data for machine learning models.

### 3. Model Selection

* Logistic Regression
* Decision Tree
* Random Forest
* Gradient Boosting

### 4. Choosing Metric

In this imbalanced loan-default problem, I prioritized recall because missing a true defaulter is more expensive than reviewing a few additional false-positive cases because missing a defaulter can lead to financial loss.

### 5. Hyperparameter Optimization

* Used GridSearchCV to improve model performance.
* Selected the best-performing model based on validation metrics.

### 6. Deployment

* Saved the trained model using Joblib.
* Built a Streamlit application for real-time loan default prediction.

-----

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-Learn
* Joblib
* Streamlit

-----

## 📊 Data Visualization

### 1. Categorical Feature Distribution
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/categorical_feature_univariate_distributions.png" width="100%">

### 2. Numerical Feature Distribution
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/numerical_feature_univariate_distributions.png" width="100%">

### 3. Categorical Features by Default
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/categorical_feature_distributions_by_default.png" width="100%">

### 4. Numerical Features by Default
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/numerical_feature_distributions_by_default.png" width="100%">

### 5. Overall Default Rate
**About 88.4% of customers have fully paid the loan while 11.6% customers have defaulted the loan.**
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/default_distribution.png" width="100%">

### 6. Default Rate — Pie Chart
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/default_pie_visualization.png" width="100%">

### 7. Credit Score vs. Default
**Credit scores look nearly identical for both successful payers and those who default on their loans.**
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/credit_score_distribution.png" width="100%">

### 8. DTI vs. Default
**A borrower's debt to income ratio shows almost no meaningful relationship between those who pay and those who default.**
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/dti_distribution.png" width="100%">

### 9. Loan Amount vs. Default
**Borrowers who are failing to repay their loans tend to request slightly larger loan amounts on average overall.**
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/loan_amount_distribution.png" width="100%">

### 10. Income vs. Default
**People who default on their loans generally earn noticeably lower annual incomes compared to successful, reliable loan payers.**
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/income_distribution.png" width="100%">

### 11. Employment Stability vs. Default
**Borrower with less employment month are tends to default more than borrower with stable employment.**
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/employment_stability.png" width="100%">

### 12. Employment Type vs. Default
**Unemployed individuals show the highest risk of defaulting, while full-time workers consistently show the lowest overall risk.**
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/employment_types.png" width="100%">

### 13. Education Level vs. Default
**Borrowers holding only a high school diploma represent the highest risk group for failing to repay their loans.**
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/education_default.png" width="100%">

### 14. Loan Purpose vs. Default
**Loans taken out for business purposes carry the highest default risk, while home loans remain the safest.**
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/default_by_loan_purpose.png" width="100%">

### 15. Correlation Heatmap before Feature Engineering
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/correlation_heatmap.png">

### 16. Correlation Heatmap after Feature Engineering
<img src="https://github.com/neuralarin/Loan-Default-Risk-Prediction-System/blob/main/images/correlation_heatmap_after_feature_engineering.png">

-----

## 📈 Baseline Summary

| Model | Accuracy | Precision | Recall | F1-score | Status / Selection |
|---|---:|---:|---:|---:|---|
| **Gradient Boosting** | **0.89** | 0.86 | **0.89** | 0.84 | 🏆 **Champion (Best Overall Performance)** |
| **Random Forest** | 0.88 | 0.85 | 0.88 | **0.85** | 🥈 **Runner-Up (Highest F1 Score)** |
| **Decision Tree** | 0.81 | 0.81 | 0.81 | 0.81 | Baseline Comparison |
| **Logistic Regression** | 0.69 | **0.86** | 0.69 | 0.74 | Highest Precision, Lower Recall |

---

## 🏆 After Hyperparameter Optimization

| Model | Recall (Class 1) | Status | 
|---|---:|---| 
| **Logistic Regression** | **69%** | 🏆 **Champion Model** | 
| Decision Tree | 63% | Good Performance | 
| Random Forest | 65% | Good Performance | 
| Gradient Boosting | 8% | Poor Performance |

-----

## 🚀 Business Impact

- Identifies high-risk borrowers before loan approval.
- Helps reduce potential credit and financial losses.
- Improves data-driven lending decisions.
- Detects ~69% of actual defaulters using the tuned model.
- Supports automated and scalable credit risk assessment.
- Strengthens the bank's overall credit risk management and portfolio stability.