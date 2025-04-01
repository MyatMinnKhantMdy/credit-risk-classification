# Credit Risk Classification

## **Background**
This project aims to use various machine learning techniques to train and evaluate a model that predicts loan risk. Using a dataset of historical lending activity from a peer-to-peer lending service, we will develop a model to determine the creditworthiness of borrowers.

## **Project Setup**
### **Repository Structure**
1. Create a new repository named **credit-risk-classification**.
2. Clone the repository to your local machine.
3. Inside the repository, create a folder named **Credit_Risk**.
4. Add the following files to the "Credit_Risk" folder:
   - `credit_risk_classification.ipynb` (Jupyter Notebook for analysis)
   - `lending_data.csv` (Dataset for training/testing the model)
5. Push all changes to GitHub.

## **Files Included**
- `credit_risk_classification.ipynb`: Jupyter Notebook for executing machine learning models.
- `lending_data.csv`: Dataset containing historical lending activity.
- `README.md`: Project documentation.

## **Instructions**
The challenge consists of the following key steps:

### **1. Split the Data into Training and Testing Sets**
- Load the `lending_data.csv` into a Pandas DataFrame.
- Create the **labels set (y)** from the `loan_status` column.
- Create the **features set (X)** from the remaining columns.
- Split the data into **training and testing datasets** using `train_test_split`.

### **2. Create a Logistic Regression Model with the Original Data**
- Fit a **Logistic Regression model** using the training data (`X_train`, `y_train`).
- Save predictions for the test set (`X_test`).
- Evaluate model performance by generating:
  - A **confusion matrix**.
  - A **classification report**.
  - An **analysis of model performance** (accuracy, precision, recall).

### **3. Write a Credit Risk Analysis Report**
- Summarize the performance of the models.
- Compare the results from:
  1. **Logistic Regression (Original Data)**
  2. **Logistic Regression (Oversampled Data)**
- Provide a recommendation on the best model for predicting loan risk.

## **Results**
### **Logistic Regression (Original Data)**
- **Accuracy:** 99%
- **Precision:**
  - Healthy Loans (0): **1.00**
  - High-Risk Loans (1): **0.84**
- **Recall:**
  - Healthy Loans (0): **0.99**
  - High-Risk Loans (1): **0.94**

### **Logistic Regression (Oversampled Data)**
- **Accuracy:** 99%
- **Precision:**
  - Healthy Loans (0): **1.00**
  - High-Risk Loans (1): **0.84**
- **Recall:**
  - Healthy Loans (0): **0.99**
  - High-Risk Loans (1): **0.99**

## **Summary and Recommendation**
- Both models achieved **99% accuracy**, but their effectiveness depends on the problem's priority.
- The original logistic regression model performs well but misses some high-risk loans (recall = 0.94).
- The **oversampled logistic regression model** improves recall for high-risk loans to **0.99**, reducing false negatives (missed risky loans), making it better for risk assessment.
- **Recommended Model:** The **oversampled logistic regression model** is preferred as it reduces missed high-risk loans, which is critical for financial risk management.

## **Conclusion**
This project applies **logistic regression** to predict loan risk and evaluates model effectiveness using **precision, recall, and accuracy metrics**. The **oversampled model is recommended** as it minimizes the risk of falsely classifying high-risk loans as safe, which is critical for lenders assessing borrower creditworthiness.
