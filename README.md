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

**Overview** 

The primary purpose of this analysis is to evaluate the performance of machine learning models in predicting the credit risk of loans, categorized as either healthy loans (0) or high-risk loans (1).

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

**Results:**
**Machine Learning Model: Logistic Regression**

- **Accuracy:** 99%
  - The model correctly classified 99% of the loans in the test dataset.

- **Precision:**
  - Healthy Loan (0): 100% - All predicted healthy loans were indeed healthy.
  - High-Risk Loan (1): 87% - 87% of the loans predicted as high-risk were actually high-risk.

- **Recall:**
  - Healthy Loan (0): 100% - All actual healthy loans were identified correctly.
  - High-Risk Loan (1): 95% - The model identified 95% of actual high-risk loans.
 
- **F1-Score:**
  - Healthy Loan (0): 100% - Perfect balance of precision and recall for the majority class.
  - High-Risk Loan (1): 91% - Strong balance of precision and recall for the minority class. 

**Summary** 

The logistic regression model achieves strong performance metrics, including a high overall accuracy of 99%, precision of 87%, and recall of 95% for identifying high-risk loans. However, despite these metrics, I would **not recommend this model as is** for deployment, or I would recommend it with the caveat that further testing and refinement are necessary.

**Concerns**

  - **Imbalanced Dataset:**
    - The dataset is heavily imbalanced, with significantly fewer high-risk loans (1) compared to healthy loans (0). This likely skews the model’s ability to generalize, as it has far more data to learn from for healthy loans than high-risk loans.
   
  - **Main Goal:**
    - The main goal is to accurately predict the credit risks of loans. While the model has a strong recall (95%) for high-risk loans, its precision for this category (87%) indicates that some healthy loans are being midclassified as high-risk.
    - Miscalssifications of this kind can lead to denial of loans to eligible individuals, which can negatively impact both the lender's reputation and the borrower's opportunities.
   
**Recommendations for Improvement**

  - **Increase the High-Risk Loan Data:**
    - Collect or generate more data for high-risk loans to balance the dataset. This will provide the model with sufficient examples of high-risk loans and help it to generalize better.
   
  - **Alternative Techniques:**
    - Use techniques like oversampling or undersampling to address the imbalance.
    - Experiment with algorithms better suited to imbalance data, like Random Forest

  - **Further Testing:**
    - Validate the model on a separate dataset with more balance proportions of high-risk and healthy loans to assess its real-world performance.

**Conclusion**

This model provides a solid starting point, but is imbalanced training data limits its utility for real-world applications. A better approach would be to refine the dataset and test additional models to ensure high-risk loans are identified with greater precision and recall. This would help the lender make more accurate decisions, ultimately improving the loan approval process. 

