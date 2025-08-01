# 🪪 Credit-Card-Defaulter-Predictor
This project presents a comprehensive ML pipeline to predict the likelihood of credit card customers defaulting on their payments. The objective is to develop an accurate, interpretable, and deployable model for binary classification — whether a customer will default (Yes/No) in the next month.

---

# 💳 Credit Default Prediction Model

This repository contains a full machine learning pipeline to predict whether a customer will default on their credit card payment in the upcoming month. The project includes data preprocessing, exploratory data analysis, feature engineering, model training, hyperparameter tuning, evaluation, and final deployment.

---

## 📁 Dataset

- **Source**: UCI Machine Learning Repository  
- **Link**: [Default of Credit Card Clients Dataset](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients)  
- **Samples**: 30,000 customers  
- **Features**:
  - Demographics: Age, Gender, Education, Marital Status
  - Credit usage: Limit, Bill Amounts (last 6 months), Payments
  - Repayment status for past 6 months
  - Target: `default payment next month` (Yes/No)

---

## 🎯 Objective

Build a predictive model that classifies whether a credit card client is likely to default in the upcoming month, helping financial institutions manage risk and take preventive measures.

---

## 📊 Exploratory Data Analysis (EDA)

- Plots: Count plots, pie charts, distribution analysis
- Detected skewness in bill and payment amounts
- Correlation analysis using heatmaps
- Feature transformation to handle non-normal distributions

---

## 🧹 Data Preprocessing

- Renamed columns for clarity (`PAY_0` → `SEP_PAY`, etc.)
- One-hot encoding for `EDUCATION` and `MARRIAGE`
- Outlier handling using IQR method
- Feature scaling using `StandardScaler`
- Target encoded as binary: `Yes = 1`, `No = 0`

---

## 🤖 Models Used

| Model                | Accuracy | Precision | Recall | F1 Score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | 0.68     | 0.69      | 0.68   | 0.68     |
| Decision Tree       | 0.82     | 0.81      | 0.83   | 0.82     |
| Random Forest       | 0.88     | 0.93      | 0.83   | 0.88     |
| AdaBoost            | 0.86     | 0.93      | 0.78   | 0.85     |
| Gradient Boosting   | 0.87     | 0.94      | 0.80   | 0.86     |

🔍 **Best model**: Random Forest (after hyperparameter tuning with GridSearchCV)

---

## 🔁 Model Deployment

- Final pipeline serialized with `joblib`
- Easily reloadable and usable for prediction on new data

## 🛠 Tech Stack
### 🔢 Languages & Libraries
- Python – Core programming language used
- NumPy – Numerical operations and array handling
- Pandas – Data manipulation and preprocessing
- Matplotlib & Seaborn – Data visualization and exploratory analysis
- imblearn (imbalanced-learn) – Handling class imbalance (e.g., SMOTE, RandomOverSampler)
- Scikit-learn – Machine learning models, preprocessing, pipelines, and evaluation
- Joblib – Model serialization and deployment

### Machine Learning & Preprocessing
- Models: Logistic Regression, Decision Tree, Random Forest, AdaBoost, Gradient Boosting
- Resampling: SMOTE (from imblearn)
- Scaler: StandardScaler
- Pipeline: sklearn.pipeline
- Model Evaluation: Accuracy, Precision, Recall, F1-Score, Confusion Matrix, Classification Report

### 🖥️ Tools & Environment
- Jupyter Notebook – Interactive development environment
- VS Code or any Python IDE – for editing and experimentation
- Git & GitHub – Version control and project sharing

## 📌 Conclusion

This project demonstrates how machine learning can be applied to real-world financial data to assess credit risk. The workflow can be extended for use in banking applications, risk dashboards, and credit scoring systems.

## **📞 Contact**
For questions, feedback, or collaboration, feel free to reach out:
Email: devikishore18@gmail.com
LinkedIn: https://www.linkedin.com/in/devikishore18/



 
