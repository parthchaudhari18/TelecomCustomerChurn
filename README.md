# Predicting Customer Attrition: A Machine Learning Approach

## Overview
Customer churn is a critical challenge for businesses, impacting revenue and growth. This project leverages machine learning techniques to predict customer churn, analyze key factors contributing to churn, and derive actionable insights for improving customer retention strategies.

## Features
- **Comprehensive Data Cleaning**: Address missing values, normalize data, and encode categorical features.
- **Exploratory Data Analysis (EDA)**: Visualizations to understand feature distributions, correlations, and relationships with churn.
- **Machine Learning Models**:
  - Logistic Regression
  - Support Vector Machine (SVM)
  - K-Nearest Neighbors (KNN)
  - XGBoost
  - Random Forest
- **Performance Metrics**: Evaluate models using accuracy, ROC-AUC, precision, recall, and F1-scores.
- **Key Insights**: Analyze feature importance and customer characteristics influencing churn.

## Dataset
The dataset contains information about customers, their subscriptions, and churn status. Key features include:
- **Demographics**: Gender, senior citizen status, dependents.
- **Subscription Details**: Contract type, monthly and total charges, tenure.
- **Services**: Internet, security, technical support, and streaming services.

## Methodology
1. **Data Preprocessing**:
   - Handle missing values by imputing `TotalCharges` with the column mean.
   - Encode categorical features using Label Encoding.
   - Scale numerical features (`MonthlyCharges`, `TotalCharges`, `tenure`) using `StandardScaler`.
   - Drop irrelevant columns like `customerID`.

2. **Exploratory Data Analysis (EDA)**:
   - Correlation heatmaps to identify relationships between features and churn.
   - Distribution plots for numerical and categorical features.
   - Feature importance analysis using Random Forest.

3. **Model Training and Evaluation**:
   - Train models on a 70-30 train-test split.
   - Evaluate using:
     - Accuracy
     - ROC-AUC
     - Confusion Matrices
     - Precision, Recall, and F1-scores.

## Results
- **Best Performing Models**:
  - Logistic Regression and Random Forest achieved the highest accuracy (79%) and ROC-AUC (95%).
- **Key Findings**:
  - Features like `SeniorCitizen`, `PhoneService`, `TotalCharges`, and `MonthlyCharges` were critical in predicting churn.
  - Tenure had an inverse relationship with churn risk.

## Visualizations
- **ROC Curves**: Model performance across multiple classes.
- **Feature Importance**: Key drivers of churn identified using Random Forest.
- **Correlation Heatmaps**: Relationships between features and churn.
- **Boxplots**: Insights into numerical features like tenure and charges.

## Challenges
- **Class Imbalance**: Significant imbalance in churn classes impacted minor class predictions.
- **Data Type Inconsistencies**: Conversion of non-numeric `TotalCharges` required careful handling.

## Future Improvements
1. **Address Class Imbalance**:
   - Implement oversampling techniques (e.g., SMOTE).
2. **Incorporate Additional Features**:
   - Customer satisfaction scores or complaint history.
3. **Time-Series Analysis**:
   - Analyze customer behavior over time for dynamic churn prediction.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/customer-churn-analysis.git
   ```
2. Navigate to the project directory:
   ```bash
   cd customer-churn-analysis
   ```
3. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the analysis:
   ```bash
   python churn_analysis.py
   ```

## Author
**Parth Chaudhari**  
This project was developed as part of an initiative to understand and mitigate customer churn using machine learning techniques.

## License
This project is licensed under the MIT License.

