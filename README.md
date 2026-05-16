# Customer Churn Prediction

A machine learning project that predicts whether a customer will churn (leave a service) based on behavioral and demographic data. Two classification models, Random Forest and Logistic Regression, are trained, evaluated, and compared.

---

## Project Overview

Customer churn is one of the most critical problems for subscription-based businesses. This project builds a complete ML pipeline from raw data to model evaluation to identify customers at risk of churning, enabling businesses to take proactive retention actions.

---

## Project Structure

```
Customer-Churn-Prediction/
│
├── Customer_Churn_Prediction.ipynb   # Main Jupyter Notebook
├── customer_churn.csv                # Dataset (input)
├── task3_eda.png                     # EDA visualizations
├── task3_confusion_matrix.png        # Confusion matrices
├── task3_feature_importance.png      # Feature importance chart
└── README.md
```

---

## Workflow

```
Load Data --> Exploratory Data Analysis --> Data Cleaning --> Feature Encoding
    --> Train/Test Split --> Model Training --> Evaluation --> Feature Importance
```

---

## Dataset

**File:** `customer_churn.csv`

| Feature | Description |
|---|---|
| Age | Customer's age |
| Subscription Type | Type of subscription plan |
| Contract Length | Monthly or Annual contract |
| Support Calls | Number of support calls made |
| Total Spend | Total amount spent by the customer |
| Churn | Target variable — 1 (Churned) / 0 (Retained) |

The CustomerID column is dropped as it holds no predictive value.

---

## Exploratory Data Analysis

Six visualizations are generated to understand churn patterns:

- Churn Distribution — Pie chart of churned vs. retained customers
- Age Distribution by Churn — Histogram with KDE
- Subscription Type vs Churn — Grouped bar chart
- Support Calls by Churn — Box plot
- Contract Length vs Churn — Grouped bar chart
- Total Spend by Churn — Box plot

---

## Data Preprocessing

- Dropped rows that are entirely null
- Removed the CustomerID column
- Filled missing numerical values with median
- Filled missing categorical values with mode
- Encoded all categorical features using Label Encoding

---

## Models Used

| Model | Library |
|---|---|
| Random Forest Classifier | sklearn.ensemble |
| Logistic Regression | sklearn.linear_model |

**Train/Test Split:** 80% training and 20% testing with stratification applied.

---

## Evaluation Metrics

Both models are evaluated using the following metrics:

- Accuracy Score
- Confusion Matrix
- Classification Report (Precision, Recall, F1-Score)

---

## Key Insights

- Support Calls and Payment Delay are the strongest predictors of churn
- Customers on monthly contracts churn significantly more than those on annual contracts
- Customers with lower total spend tend to churn more often

---

## Tech Stack

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

---

## Getting Started

**1. Clone the Repository**

```bash
git clone https://github.com/SyedAfzaalShah/Customer-Churn-Prediction.git
```

**2. Install Dependencies**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

**3. Add the Dataset**

Place `customer_churn.csv` in the project root directory.

**4. Run the Notebook**

```bash
jupyter notebook Customer_Churn_Prediction.ipynb
```

---

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---
