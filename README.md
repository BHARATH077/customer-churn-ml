# Customer Churn Prediction 🚀

## 📌 Project Overview
This project predicts customer churn for a telecom company using machine learning.  
It simulates an end-to-end workflow: from data collection and preprocessing to model training, evaluation, explainability, and deployment.

## 📂 Dataset
We are using the **Telco Customer Churn dataset** from Kaggle.  
Source: [Kaggle Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

- Filename: `data/WA_Fn-UseC_-Telco-Customer-Churn.csv`
- Records: 7,043 customers
- Target variable: `Churn` (Yes/No)

## 🔄 Workflow
1. **Data Cleaning & EDA** – Handled missing values, visualized churn patterns.  
2. **Feature Engineering** – Encoded categorical variables, scaled numerical ones.  
3. **Modeling** – Logistic Regression baseline, Random Forest, and XGBoost.  
4. **Hyperparameter Tuning** – RandomizedSearchCV for optimization.  
5. **Explainability** – SHAP and LIME to interpret predictions.  
6. **Deployment** – Flask API to serve churn predictions.  

## 📊 Results
- Logistic Regression baseline: **74% accuracy**, Recall (churn): **0.78**  
- Tuned XGBoost: **ROC-AUC: ~0.85**, Best recall for churn class  
- Key features driving churn: **Contract type, tenure, monthly charges, internet service**  

## 🛠 Tech Stack
- Python, Pandas, NumPy, Scikit-learn, XGBoost  
- SHAP, LIME for explainability  
- Flask for deployment  
- Matplotlib & Seaborn for visualization  

## 🚀 Demo
Example API request:
```bash
curl -X POST http://127.0.0.1:5000/predict \
-H "Content-Type: application/json" \
-d '{"gender":"Female","InternetService":"Fiber optic","Contract":"Month-to-month","tenure":5,"MonthlyCharges":80,"TotalCharges":400}'



