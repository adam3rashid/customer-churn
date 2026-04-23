# 📉 Customer Churn Analysis & Prediction

A machine learning project analyzing customer attrition data from a telecommunications provider to identify patterns that lead to churn and build a predictive model.

---

## Project Objective

The goal of this project is to analyze customer data to **identify patterns that lead to customer attrition (churn)**. By understanding these factors, we aim to:

- Build a **predictive machine learning model** that identifies at-risk customers
- Provide **actionable insights** to implement targeted retention strategies
- Understand which customer segments are most vulnerable to churn

---

## Key Research Questions

1. Which **demographic factors** (gender, seniority, partners) are most associated with churn?
2. How do **service features** (internet type, technical support, streaming) impact customer loyalty?
3. What is the relationship between **financial metrics** (monthly charges, tenure) and the likelihood of leaving?

---

## Dataset

The dataset used is the **IBM Telco Customer Churn** dataset (`WA_Fn-UseC_-Telco-Customer-Churn.csv`), containing **7,043 customer records** with **21 features**.

### Features include:
| Category | Features |
|---|---|
| **Demographics** | `customerID`, `gender`, `SeniorCitizen`, `Partner`, `Dependents` |
| **Account Info** | `tenure`, `Contract`, `PaperlessBilling`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges` |
| **Services** | `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies` |
| **Target** | `Churn` (Yes/No) |

---

## Tech Stack

| Tool | Purpose |
|---|---|
| **Python** | Core language |
| **Pandas** | Data manipulation and analysis |
| **NumPy** | Numerical operations |
| **Matplotlib** | Data visualization |
| **Seaborn** | Statistical data visualization |
| **Scikit-learn** | Machine learning models |
| **Jupyter Notebook** | Interactive development environment |

---

## Project Structure

```
customer-churn/
├── CustChurnPredictionDS.ipynb     # Main analysis notebook
├── WA_Fn-UseC_-Telco-Customer-Churn.csv  # Dataset (not tracked)
└── README.md                       # Project documentation
```

---

## Analysis Workflow

### 1. Data Loading & Exploration
- Load dataset and inspect structure
- Check data types and null values
- Review descriptive statistics

### 2. Exploratory Data Analysis (EDA)
- **Churn Distribution** — examine class imbalance
- **Monthly Charges vs Churn** — price sensitivity analysis
- **Tenure vs Churn** — customer loyalty patterns
- **Contract Type vs Churn** — impact of contract length
- **Internet Service vs Churn** — service type analysis
- **Payment Method vs Churn** — billing preferences

### 3. Data Cleaning
- Convert `TotalCharges` from string to numeric
- Drop rows with null values (~11 rows)
- Remove non-predictive columns (`customerID`)

### 4. Feature Engineering & Preprocessing
- Label encoding of categorical variables
- Feature scaling / normalization

### 5. Model Training & Evaluation
- Train/test split
- Model comparison (Logistic Regression, Decision Tree, Random Forest, etc.)
- Evaluation metrics: Accuracy, Precision, Recall, F1-Score, AUC-ROC

---

## Key Insights

- **High monthly charges** are correlated with higher churn — price-sensitive customers leave more readily
- **Short tenure** is strongly associated with churn — early-stage customers are the most at-risk
- **Month-to-month contracts** show the highest churn rates vs. annual or two-year contracts
- **Fiber optic** internet users exhibit higher churn, potentially due to cost or service expectations

---

## Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Run the Notebook
```bash
jupyter notebook CustChurnPredictionDS.ipynb
```

> **Note:** The dataset file (`WA_Fn-UseC_-Telco-Customer-Churn.csv`) must be placed in the same directory as the notebook.

---

## Future Improvements

- [ ] Apply SMOTE or other resampling techniques to address class imbalance
- [ ] Hyperparameter tuning with GridSearchCV / RandomizedSearchCV
- [ ] Build a simple Flask/Streamlit dashboard for real-time churn prediction
- [ ] Explore deep learning approaches (e.g., neural networks)
- [ ] Deploy model to a cloud endpoint

