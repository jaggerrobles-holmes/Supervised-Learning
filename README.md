# 📊 Credit Risk Prediction using Logistic Regression & Random Forest
This project analyzes loan applicant data to predict credit risk using supervised learning. By applying logistic regression and random forest models, we identify key factors influencing loan defaults and optimize for detecting high-risk borrowers while minimizing false alarms.

---

## 🎯 Project Objective

**Can we predict which loan applicants are most likely to default?**
Using historical data, I built a model that flags high-risk applicants while maintaining fairness in approval rates.

---

## 📁 Dataset

**Source**: [Kaggle - credit_risk_dataset.csv](https://www.kaggle.com/datasets/laotse/credit-risk-dataset?resource=download&select=credit_risk_dataset.csv)
**Size**: 32,581 loan applications
**Key Features**:
Applicant income, loan amount, interest rate
Credit history, employment length, loan purpose
Home ownership status

---

## 🧠 Methods

##### 1. Data Preprocessing
Handled missing values (loan_int_rate, person_emp_length)
Capped extreme values (e.g., age > 80 → 80)
Engineered features:
income_loan_ratio (income divided by loan amount)
high_risk_purpose (flag for medical/debt consolidation loans)

##### 2. Models Compared
| Model |	Accuracy | Specificity (Default Detection) |	AUC |
|-------|----------|---------------------------------|------|
| Logistic Regression|	82.4% |	34.0% |	0.77 |
| Balanced Random Forest |	83.5% |	54.5% |	0.80 |

##### 3. Key Tools
**Data Cleaning**: dplyr, tidyr
**Visualization**: ggplot2
**Machine Learning**: caret, randomForest
**Evaluation**: ROC curves, confusion matrices

---

## 🔎 Key Findings
**Top Default Risk Factors**
High Interest Rates (Strongest predictor)
Low Income-to-Loan Ratios
Debt Consolidation/Medical Loans

**Model Trade-offs**
Random Forest caught 54.5% of defaults (vs 34% for logistic regression)
**Cost**: Increased false positives (539 vs 263)

**Undervalued Insights**
Renters had 2x higher default rates than homeowners
Short credit histories (<3 years) showed elevated risk

---

## 💡 Business Impact
By prioritizing the random forest model:
**Detects 20% more defaults than traditional methods**
**Could reduce bank losses by thousands to millions of dollars**

---

## 📦 Files
**Credit_Risk_Project.Rmd**: Full R markdown with analysis
**credit_risk_dataset.csv**: Raw dataset
**Credit_Risk_Project.html**: HTML of completed project with visualizations
**README.md**: This file

---

## 📈 Future Improvements
Experiment with thresholds (e.g., 0.3 instead of 0.5) to optimize for risk tolerance
Add alternative data (e.g., rent payment history)
Deploy as API for real-time risk scoring

---

```bash
git clone https://github.com/jaggerrobles-holmes/Credit_Risk_Project.git
cd Credit_Risk_Project
R Markdown


