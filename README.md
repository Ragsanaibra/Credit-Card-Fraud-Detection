# Credit-Card-Fraud-Detection
This project aims to automatically detect fraud through analysis of credit card transactions.
## Project Report
### 1. Problem Definition
Project Goal: The aim of this project is to detect fraudulent transactions in credit card operations. The goal is to identify suspicious transactions at an early stage to minimize financial losses for both banks and users.

Type of Machine Learning: This is a classification problem. The model must classify each transaction as either “fraud” or “normal”.

Expected Outcome: Accurately predict whether a transaction is fraudulent or not. The goal is to ensure effective detection with high precision, recall, and F1-score.

### 2. Data Collection & Understanding
Source: The dataset is publicly available on the Kaggle platform under the “Credit Card Fraud Detection” dataset.

Link: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Dataset Description:

Rows (transactions): Approximately 284,807

Number of Columns: 31 (Time, V1–V28, Amount, Class)

Key Statistics & Visualization:

Class Imbalance:

Class = 0 (normal) ≈ 99.8%

Class = 1 (fraud) ≈ 0.2%

This imbalance poses challenges in model training and requires special handling techniques such as SMOTE or using class_weight.

### 3. Data Cleaning & Preprocessing
NaN and Missing Values: There are no NaN or missing values in the dataset.

Categorical Variables: All features are numerical — no encoding is required.

Feature Scaling and Normalization:

StandardScaler was applied to the Time and Amount columns.

Initially, Amount and Time had different scales; after scaling, they were normalized for model input.

### 4. Feature Engineering
New Features: No additional features were created.

Removing Irrelevant Features: All existing features were retained.

Feature Selection & Dimensionality Reduction:

No further reduction was applied.

The dataset already uses PCA-reduced features (V1–V28).

### 5. Model Training
Machine Learning Algorithms Used:

Logistic Regression

Random Forest Classifier

Target Variable: Class (0 = normal, 1 = fraud)

Model Comparison:

Both models were trained and their results were compared.

### 6. Model Evaluation
Evaluation Metrics:

Accuracy, Precision, Recall, F1-score, ROC-AUC

Comparison:

Logistic Regression is simple but provides poor recall due to the class imbalance.

Random Forest achieved better performance overall.

Cross-Validation:

Yes, k-fold cross-validation was applied.

### 7. Model Improvement
Hyperparameter Tuning:

Used GridSearchCV to tune parameters like n_estimators and max_depth for Random Forest.

Additional Preprocessing or Feature Selection:

Techniques such as SMOTE and class_weight were used to address class imbalance.

Impact on Results:

The improved model produced more stable results in terms of F1-score and Recall.

### 8. Final Model & Report
Best Performing Model:

Random Forest Classifier — was able to correctly identify more fraudulent transactions.

Overall Summary of Results:

The project successfully tackled a highly imbalanced classification problem using appropriate methods and modeling techniques.
