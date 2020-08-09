# Hackathon-Loan
>Analytics Vidya Hackathon

# Project Background
### Problem Addresssed -
This Project addresses the problem of sanctioning loans to potential clients.Sanctioning loans with proper care will help company in preventing Non-Performing Assets(Bad  Loans).NPA's are a major concern for the banks as they not only lead to reduction in profits but also are a reason for strict regulations by Central Banks.
### Solution offered-
This Machine Learning algorithm helps in classifying whether an applicant is eligible for a loan. This in turn help in reducing the NPA's and lead to better bottomline. 

# About the Dataset
The Dataset contains 12 Independent Features and 1 Dependent Feature(Loan_Status) which are described as follows-
- Loan_ID-	Unique Loan ID of every applicant.
- Gender-	Male/ Female of the applicant.
- Married-	Marital Status of the applicant.
- Dependents-	Number of dependents of the applicant.
- Education-	Applicant Education (Graduate/ Under Graduate).
- Self_Employed-	Whether the applicant is Self employed (Y/N).
- ApplicantIncome-	Applicant's income.
- CoapplicantIncome-	Coapplicant's income.
- LoanAmount-	Loan amount seeked(in thousands).
- Loan_Amount_Term-	Term of loan in months.
- *Credit_History -	Credit history meets guidelines.
- Property_Area-	Urban/ Semi Urban/ Rural.
- Loan_Status-	(Target) Loan approved (Y/N).


*Note 1- Here in the dataset the 'Credit_History' feature is just a binary column . However in reality there is a Credit Score which is given by a Credit Rating Agency on the basis of past payment records of a person. This Credit Score provided is an essential factor for providing a loan.

*Note 2-Here there are 12 features considered for classifying. However in reality we can add as many as we want. Generally all of the above information is obtained when the company is performing the KYC of any applicant.

# Steps used during the project
1) Exploratary Data Analysis- 
  - Correlation with Target Variable
  - Countplot to know the Target Variables distribution
  - Distplot to check the skewness of every Continous Feature
  - Stacked Bar plot to know the count of every Categorical Feature with respect to the Target Feature
  
 2) Preprocessing and Feature Engineering -
  - Filling missing values
  - Dealing with the Skewness of the data by using scalers
  - Adding new Features to the Dataset
  - Scaling the continous columns
  - One hot Encoding on the categorical columns
  
  3) Applying models-
  - The problem is a Classfication problem where 0 indicates Loan is not Approved and 1 indicates Loan is approved
  - Various models were used on the above data
  - The best two performing were the Catboost Classifier and the Stacking Ensemble Classification Method
  
  4) Evaluation Metric-
   
     Model performance was evaluated on the basis of the prediction of loan status and the metric to judge it was Accuracy.
   
   - Evaluation for Catboost Classifier-
     Test score is  0.8292682926829268,
     Precision score is 0.822429906542056,
     Recall score is 0.9777777777777777,
     Confusion Matrix is 
      [[14,19]
      [2,88]]
      
   - Evaluation for Ensemble Classifier-
     Test score is  0.8292682926829268,
     Precision score is 0.8349514563106796,
     Recall score is 0.9555555555555556,
     Confusion Matrix is 
      [[16,17]
      [4,86]]
      
