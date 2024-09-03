
                                       Project Name :  Financial Risk Assessment

### 1. Introduction

The objective of this project was to assess financial risk by analyzing a dataset that includes various customer attributes and loan-related information. The data was used to build a predictive model to evaluate the risk rating of loan applications.

### 2. Data Description

The dataset contains the following features:

- # Categorical Features:
  - Gender
  - Education Level
  - Marital Status
  - Loan Purpose
  - Employment Status
  - Payment History
  - City
  - State
  - Country

- # Numerical Features:
  - Age
  - Income
  - Credit Score
  - Loan Amount
  - Years at Current Job
  - Debt-to-Income Ratio
  - Assets Value
  - Number of Dependents
  - Previous Defaults

The target variable for the model is **Risk Rating**, which is a categorical variable representing the risk level of a loan application.

### 3. Data Preprocessing

#### 3.1. Handling Missing Values

- **Categorical Variables:** Missing values were imputed using the most frequent value within each column.
- **Numerical Variables:** Missing values were imputed with the mean value of the respective columns.

#### 3.2. Encoding Categorical Variables

Categorical features were encoded using One-Hot Encoding to convert them into a format suitable for machine learning models. The `ColumnTransformer` was employed to handle both categorical and numerical data transformations:

- # One-Hot Encoding: Applied to categorical features, excluding the first category to avoid multicollinearity.
- # Feature Scaling: Numerical features were standardized using `StandardScaler` to ensure all features contribute equally to the model.

#### 3.3. Feature Engineering

- Features were transformed into a sparse matrix format and then converted into a dense DataFrame for modeling.

### 4. Machine Learning Model

#### 4.1. Model Selection

- A Random Forest Classifier was chosen for this project due to its robustness and ability to handle both numerical and categorical data effectively. 

#### 4.2. Training and Testing

- The data was split into training (70%) and testing (30%) sets.
- The Random Forest model was trained on the training set and evaluated on the test set.

### 5. Model Evaluation

#### 5.1. Confusion Matrix

The confusion matrix shows the number of true positive, true negative, false positive, and false negative predictions for each class, providing insights into the model's performance.

#### 5.2. Feature Importance

Feature importance scores were calculated to determine which features had the most influence on the model's predictions. 

The chart highlights the features that significantly impact the risk rating predictions.


### 6. Conclusion

The Random Forest Classifier effectively assessed financial risk based on the given dataset. The preprocessing steps, including handling missing values and encoding categorical variables, were crucial for preparing the data for modeling. The evaluation metrics, including the confusion matrix, feature importance, demonstrated the model's performance and the significance of various features.
