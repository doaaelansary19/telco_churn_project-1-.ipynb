📊 Telco Customer Churn Prediction

📌 Project Overview

This project aims to predict whether a telecom customer is likely to Churn (leave the company) based on customer information and service usage.

The project follows a complete Machine Learning workflow:

Data Loading → Data Cleaning → Exploratory Data Analysis → Preprocessing → Model Training → Evaluation → Model Selection → Interpretation

🎯 Objective

The main goal is to build a classification model that can identify customers who are likely to leave the company.

The target variable is:

"0" → No Churn
"1" → Churn
🗂️ Dataset

The dataset contains information about telecom customers, including:

Customer demographics
Contract type
Internet service
Payment method
Tenure
Monthly charges
Total charges
Churn status
The dataset contains 7,043 customers and 21 columns before preprocessing.

🧹 Data Cleaning

The following steps were performed:

Removed "customerID" because it is an identifier and does not provide useful predictive information.
Converted "TotalCharges" from text to numeric values.
Converted invalid/blank values in "TotalCharges" to missing values.
Checked for missing values.
Converted "Churn" from "Yes/No" into "1/0".
Treated "SeniorCitizen" as a categorical feature.
📊 Exploratory Data Analysis

Several visualizations were used to understand the relationship between customer characteristics and churn.

Categorical Features

Count plots were used to investigate churn across:

Gender
Partner status
Senior citizen status
Contract type
Internet service
Payment method
Numerical Features

Box plots were used to compare:

Monthly Charges
Total Charges
The relationship between tenure and churn was also investigated by grouping customers into tenure ranges.

⚙️ Data Preprocessing

The dataset was divided into:

80% Training data
20% Testing data
"stratify" was used to preserve the churn distribution in both datasets.

Categorical features were encoded using:

OneHotEncoder

Numerical features were scaled using:

StandardScaler

Missing "TotalCharges" values were filled using the mean calculated from the training data.

🤖 Machine Learning Models

Three classification algorithms were trained and compared:

Logistic Regression
K-Nearest Neighbors (KNN)
Random Forest
Because the churn classes are imbalanced, "class_weight='balanced'" was used for Logistic Regression and Random Forest.

📈 Evaluation Metrics

The models were evaluated using:

Accuracy
Precision
Recall
F1-Score
ROC-AUC
The main selection metric was F1-Score for the Churn class, because detecting customers who are likely to leave is important and accuracy alone may be misleading with imbalanced data.

📉 Model Analysis

The project includes:

Model comparison chart
ROC curves
Confusion matrix
Feature importance / model coefficients
The confusion matrix helps identify:

True Positives
True Negatives
False Positives
False Negatives
💡 Conclusion

The project demonstrates a complete end-to-end Machine Learning classification workflow for customer churn prediction.

The best model was selected based on the F1-Score for the Churn class, while other evaluation metrics and visualizations were also considered to understand the model's performance.

🛠️ Technologies Used

Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Jupyter Notebook / Google Colab
📁 Project Structure

telco-customer-churn-prediction/ │ ├── telco_churn_project.ipynb └── README.md
