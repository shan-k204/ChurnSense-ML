# 🚀 ChurnSense-ML
### Predictive Customer Churn Analysis using Supervised Machine Learning

---

# 📌 Overview

ChurnSense-ML is a supervised machine learning project focused on predicting customer churn — identifying whether a customer is likely to leave or cancel a service subscription based on demographic and service-related behavior.

Customer churn prediction helps businesses:
- improve customer retention,
- reduce revenue loss,
- and make data-driven decisions.

This project demonstrates a complete end-to-end machine learning workflow including:
- Data preprocessing
- Exploratory Data Analysis (EDA)
- Correlation analysis
- Feature engineering
- Feature scaling
- Multiple classification models
- Hyperparameter tuning using GridSearchCV
- Model evaluation & comparison

The final model was selected based on predictive performance and generalization ability.

---

# 🎯 Objective

The objective of this project is to:
> Predict whether a customer will churn using supervised classification algorithms and identify behavioral patterns contributing to customer attrition.

---

# 🧠 Problem Type

| Category | Type |
|---|---|
| Machine Learning Type | Supervised Learning |
| Task | Binary Classification |
| Target Variable | Churn |

### Target Variable Meaning
- **Yes** → Customer leaves the service
- **No** → Customer stays with the service

---

# 🗂️ Dataset Information

The dataset contains customer-related information such as:
- Age
- Gender
- Tenure
- Internet Service
- Contract Type
- Monthly Charges
- Churn Status

### Target Column
```python
Churn
```

---

# ⚙️ Technologies & Libraries Used

## Programming Language
- Python

## Libraries
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

# 🔄 Machine Learning Workflow

## 1️⃣ Data Loading & Inspection

The dataset was loaded into a Pandas DataFrame to:
- understand dataset structure,
- inspect data types,
- identify missing values,
- and verify the target variable.

---

## 2️⃣ Data Preprocessing

Several preprocessing techniques were applied before model training.

### ✔ Missing Value Handling
- Around 300 missing values were detected in the `InternetService` column.
- Missing categorical values were handled using `fillna()`.

### ✔ Duplicate Check
- Duplicate records were checked to maintain data integrity.

### ✔ Feature Selection
Selected features:
- Age
- Gender
- Tenure
- MonthlyCharges

### ✔ Feature Encoding
Categorical values were converted into numerical format:
- Female → 1
- Male → 0
- Churn Yes → 1
- Churn No → 0

### ✔ Feature Scaling
`StandardScaler` was applied to normalize feature ranges.

---

# 📊 Exploratory Data Analysis (EDA)

EDA was performed to understand customer behavior and churn-related patterns.

## Visualizations Included
- Churn Distribution Pie Chart
- Contract Type vs Monthly Charges
- Monthly Charges Histogram
- Tenure Histogram

## Insights
- Customers with lower tenure showed higher churn tendency.
- Contract types influenced average monthly charges.
- Churn distribution helped analyze class balance.

---

# 🔍 Correlation Analysis

Correlation analysis was performed on numerical features to:
- understand feature relationships,
- identify dependencies,
- and detect multicollinearity.

---

# 🤖 Machine Learning Models Used

| Model | Purpose |
|---|---|
| Logistic Regression | Baseline binary classifier |
| KNN | Distance-based classification |
| SVM | Margin optimization classification |
| Decision Tree | Rule-based classification |
| Random Forest | Ensemble learning & overfitting reduction |

---

# 🛠 Hyperparameter Tuning

`GridSearchCV` with cross-validation was used to optimize model parameters and improve predictive performance.

---

# 📈 Model Performance

| Model | Accuracy |
|---|---|
| Logistic Regression | ~90% |
| KNN | ~88% |
| SVM | ~90% |
| Decision Tree | ~90% |
| Random Forest | **~91.5%** ✅ |

---

# 🏆 Final Model Selection

## ✅ Random Forest Classifier

Random Forest achieved the best overall accuracy and demonstrated strong generalization performance due to ensemble learning and reduced overfitting.

---

# 📌 Conclusion

This project successfully predicts customer churn using supervised machine learning techniques by combining:
- preprocessing,
- exploratory analysis,
- feature engineering,
- and multiple classification models.

The final Random Forest model achieved the best predictive performance.

---

# 🚀 Future Improvements

Possible enhancements include:
- ROC-AUC & F1-score evaluation
- SMOTE for class imbalance handling
- Feature importance visualization
- Model deployment using Flask or Streamlit
- Real-time churn prediction dashboard
