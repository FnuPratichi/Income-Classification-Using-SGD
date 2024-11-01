# Income Classification Using SGD

## Problem Statement
- This project addresses the problem of predicting whether an individual's yearly income exceeds $50,000 .
- The dataset utilized for this classification task is the "Adult" dataset from the UCI Machine Learning Repository.
- Each instance in the dataset corresponds to an individual and includes 
- The goal is to classify the income as either less than or equal to $50,000 (denoted as -1) or greater than $50,000 (denoted as 1).

## Dataset Details
- **Source**: UCI Machine Learning Repository
- **Name**: Adult Income Dataset
- **Target Variable**: The income class (binary) indicating whether an individual's income exceeds $50,000.
- **Attributes** : age, occupation, education level, marital status, relationship status, race, sex, capital gain, capital loss, hours worked per week, and native country.

## Steps Done
### 1. Featured the Data
- **Data Cleaning**: Removed features that were not relevant for modeling and dropped instances with missing data.
- **Encoding**: Transformed categorical variables using One-Hot Encoding to represent them as numerical values, while keeping numerical variables as is.
- **Standardization**: Applied `StandardScaler` to normalize numerical features for better model performance.
- **Feature Count**: After preprocessing, the data was transformed into **95 features**, including an intercept term.

### 2. Handled Imbalanced Dataset
- **Class Distribution Analysis**: The initial class distribution was assessed, revealing that approximately 75.2% of the instances earned less than or equal to $50,000, indicating an imbalanced dataset.
- **Class Weights**: Implemented class weights during model training to mitigate the impact of class imbalance, allowing the model to give more attention to the minority class.


### 2. Classification
- **Data Splitting**: Divided the dataset into training (80%), validation (10%), and test (10%) sets.
- **Model Training**: Implemented Logistic Regression using Stochastic Gradient Descent (SGD) to minimize the logistic loss function.
- **Gradient Calculation**: Derived the gradient of the logistic loss function for a single training example.

### 3. Hyperparameter Tuning
- Explored and optimized key hyperparameters, including:
  - **Regularization parameter (λ)**
  - **Learning rate (η)**
  - **Number of iterations**
- Employed a "guess and check" method to iteratively adjust parameters based on model performance.

### 4. Model Evaluation
- **Accuracy Calculation**: Developed functions to compute the training and test accuracy of the model.
- **Final Results**: Achieved a test accuracy of **75.17%**, validating the effectiveness of the model.

## Conclusion
- This project successfully demonstrates the use of Logistic Regression and Stochastic Gradient Descent for binary classification of income levels.
- Through thorough data preprocessing, effective feature engineering, and careful hyperparameter tuning, the model is able to predict income with a commendable accuracy of 75.17%.

