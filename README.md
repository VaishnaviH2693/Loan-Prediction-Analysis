# Loan-Prediction-Analysis
A beginner-friendly loan prediction project using Python and Power BI. The data is cleaned, analyzed, and used to train a Decision Tree model to predict loan approval. Results are exported to Power BI, where an interactive dashboard shows loan status, credit score trends, and model accuracy.

# Dataset
The dataset contains around 500 rows with features such as:

- Income
- Credit Score
- Loan Amount
- Employment Status
- Repayment History
- Loan Status (Target)

1. Data Preprocessing

- Load dataset using pandas
- Handle missing values
- Encode categorical features
- 
# Perform basic EDA
- .head()
- .info()
- .describe()
- value counts
- Prepare features (X) and target (y)

2. Machine Learning Model (Python)

A Decision Tree Classifier is used due to its simplicity and interpretability.

- Training Workflow
- from sklearn.model_selection import train_test_split
- from sklearn.tree import DecisionTreeClassifier
- from sklearn.metrics import accuracy_score


Steps:

- Split data (train/test)
- Train model
- Predict on test data
- Calculate accuracy
- Export predictions to CSV

 3. Export for Power BI

- Predictions are saved as:
- loan_prediction_output.csv
- This file contains:
- Actual Loan Status
- Predicted Loan Status

 4. Power BI Dashboard

The dashboard includes:
- Loan Status Distribution
- Income vs Loan Amount
- Credit Score Analysis
- Actual vs Predicted Comparison

# Accuracy Card using DAX

Accuracy DAX Measure
Accuracy =
DIVIDE(
    COUNTROWS(
        FILTER('loan_prediction_output',
            'loan_prediction_output'[Actual_Loan_Status] =
            'loan_prediction_output'[Predicted_Loan_Status])
    ),
    COUNTROWS('loan_prediction_output')
)

 # Conclusion:
This project demonstrates a complete end-to-end workflow from data preprocessing to machine learning and data visualization. It is ideal for beginners and students who want to build a simple and clean ML + Power BI project.
