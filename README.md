# Motor Insurance Claims Prediction and Dashboard

## Project Description
This project aims to predict motor insurance claims using machine learning models such as Logistic Regression and Random Forest. The objective is to provide actionable insights to insurers through an interactive Power BI dashboard. The project includes data preprocessing, feature engineering, model evaluation, and dashboard creation to aid in risk assessment and decision-making.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Preprocessing](#data-preprocessing)
3. [Model Training and Evaluation](#model-training-and-evaluation)
4. [Feature Importance](#feature-importance)
5. [Power BI Dashboard](#power-bi-dashboard)
6. [How to Run the Code](#how-to-run-the-code)
7. [Results and Insights](#results-and-insights)
8. [Acknowledgments](#acknowledgments)


#### Project Overview
**Dataset**: The dataset contains features such as `VehAge`, `Exposure`, `DrivAge`, and `Region`, along with the target variable `Claim`.
**Tools Used**:
- **Python**: Pandas, Numpy , Matplotlib, Seaborn, SMOTE.
- **Power BI**: Interactive dashboard for visualizing predictions and insights.


## Data Preprocessing
The following steps were performed to prepare the data:
1. **Handling Missing Values**: All missing or invalid values were addressed.
2. **Feature Encoding**: Categorical features were encoded using One-Hot Encoding.
3. **Scaling**: Numerical features like `Exposure` were normalized.
4. **Class Imbalance Handling**: SMOTE was used to balance the `Claim` class.
   
**code**:
from imblearn.over_sampling import SMOTE
smote = SMOTE(random_state=42)
X_balanced, y_balanced = smote.fit_resample(X, y)


## Model Training and Evaluation
Two machine learning models were trained and evaluated:
1. **Logistic Regression**:
   - Simple baseline model.
2. **Random Forest**:
   - High-performance model with feature importance extraction.

**Metrics**:
- Accuracy
- Precision, Recall, F1-Score
- ROC-AUC Score

**Code**:
from sklearn.ensemble import RandomForestClassifier
rf_model = RandomForestClassifier(random_state=42)
rf_model.fit(X_train, y_train)


## Feature Importance
Feature importance was calculated using the Random Forest model to identify the most influential features in predicting claims.

**Top Features**:
1. `VehAge`
2. `VehPower`
3. `Exposure`
4. `DrivAge`

**Visualization**:
A bar chart was created to display feature importance.

## Power BI Dashboard
An interactive dashboard was created in Power BI to visualize insights from the analysis.

**Dashboard Highlights**:
1. **Model Performance Comparison**: Compares Logistic Regression and Random Forest metrics.
2. **Confusion Matrix**: Displays predictions from Random Forest.
3. **Claims by Region**: Highlights claim distribution across regions.
4. **Feature Importance**: Shows the top predictors of claims.

![Dashboard Screenshot][Power BI dashboard-image.png](https://github.com/Manisha-Singh1/Motor-Insurance-Claims-Prediction-and-Dashboard/blob/main/Power%20BI%20dashboard-%20image.png?raw=true)

## How to Run the Code
1. Clone this repository:
   git clone [https://github.com/your-repo/motor-insurance-claims.git](https://github.com/Manisha-Singh1/Motor-Insurance-Claims-Prediction-and-Dashboard)

2. Install the required dependencies:
   pip install -r requirements.txt

3. Run the Jupyter Notebook:
   jupyter notebook Motor_Insurance.ipynb

4. View the Power BI dashboard:
   -Open the France Motors Insurance PB dashboard.pbix file in Power BI Desktop.


## Results and Insights
1. **Model Performance**:
   - Random Forest outperformed Logistic Regression with a higher ROC-AUC score of 0.99.
2. **Feature Importance**:
   - `VehAge` and `Exposure` were identified as the most significant predictors.
3. **Dashboard Usability**:
   - The Power BI dashboard provides actionable insights for insurers to reduce risk and optimize policies.


## Acknowledgments
- Dataset: [Motor Insurance Dataset]([https://www.kaggle.com/datasets](https://www.kaggle.com/datasets/floser/french-motor-claims-datasets-fremtpl2freq))
- Tools: Python, Power BI
- Libraries: Pandas, Numpy , Matplotlib, Seaborn, SMOTE

