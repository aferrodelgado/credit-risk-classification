# credit-risk-classification
Module 20 - Supervised Learning
<br><br>

**Instructions**

The instructions for this Challenge are divided into the following subsections:

  - Split the Data into Training and Testing Sets
  - Create a Logistic Regression Model with the Original Data
  - Write a Credit Risk Analysis Report

**Split the Data into Training and Testing Sets**

Open the starter code notebook and use it to complete the following steps:

  1. Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
  2. Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
     
     > **note:**
     > A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
  4. Split the data into training and testing datasets by using train_test_split.

**Create a Logistic Regression Model with the Original Data**

Use your knowledge of logistic regression to complete the following steps:

  1. Fit a logistic regression model by using the training data (X_train and y_train).
  2. Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
  3. Evaluate the model’s performance by doing the following:
     - Generate a confusion matrix.
     - Print the classification report.
  4. Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

<br><br>
**Credit Risk Analysis Report**

**An overview of the analysis:** The primary purpose of this analysis is to evaluate the performance of machine learning models in predicting the credit risk of loans, categorized as either healthy loans (0) or high-risk loans (1).

The dataset contains financial information about loans, including variables such as loan amount, interest rate, annual income, and loan status (loan_status). The target variable, loan_status, has two possible values:

  - 0: Healthy Loan - indicating the loan is likely to be repaid.
  - 1: High-Rish Loan - indicating the higher likelihood of default.

    **Loan Variables:** The loan_status variable is imbalanced, with significantly more healthy loans (0) than high-risk loans (1).

      - Value counts of target variable:
        - 0 (Healthy Loans): 18,759
        - 1 (High-Risk Loans): 625

    **Machine Learning Process:** The analysis involved the following steps:

    1. **Data Preprocessing:**
       - Standardized the features using StandardScaler to ensure all variables have comparable scales.
       - Split the dataset into training and testing sets.
    2. **Model Selection:**
       - Implemented and evaluated a logistic regression model (LogisticRegression) for binary classification tasks.
    3. **Model Evaluation:**
       - Used metrics such as accuracy, precision, recall, and F1-score to assess model performance, with a focus on predicting high-risk loans (1).

**The results:**

Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.
**A summary:** Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.


