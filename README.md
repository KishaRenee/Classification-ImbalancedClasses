# Classification-ImbalancedClasses

This is a Machine Learning project using Python where we are predicting if customers will subscribe (Yes/No) to a bank term deposit based on their customer attributes. Since, the target variable is discrete this will be a classification problem.
  •	 Imbalanced Classes addressed using an over-sampling technique called SMOTE.
  •	Performance metric used : AUC.
  
ML Pipeline / Methodology for Model Building
Steps :
1.	Problem Definition
2.	Data Collection
    •	Dataset : Boston Housing Market readily available
3.	Data Preparation
(i) Data Exloration & Analysis
(ii) Data Cleaning
(iii) Split into Train and Test
(iv) Feature Generation &/Or Feature Selection

   - For Logistic Regression we drop redundant features 
     using VIF & we subset features based on Feature 
     Importance ranking using Random Forest.
     Both subset of features are used to train the Logistic 
     Regression model.

   - Note, however, all other models are trained with all 
     features. 
     
(v) Data Preprocessing
   - Scale features where appropriate

4.	Train Model
5.	Validate Model & Tune Model hyperparameters
6.	Test Model assumptions (Eg. assumptions of logistic regression model)
7.	Select best model
8.	Report results
9.	Conclusion



What’s the imbalanced class problem ?
It is an issue that arises when a dataset has the number of instances skewed towards one class versus another. This creates an “imbalance” of the classes which biases the model towards that majority class. 
To address this, we can use an over-sampling technique called SMOTE (Synthetic Minority Over-Sampling) technique.

What is SMOTE?
Synthetic Minority Over-Sampling (SMOTE) is a technique which oversamples from the minority class using synthetic instances. These synthetic instances are created with similar features to the actual instances. Each synthetic instance is a variant of the k-closest neighbors to a particular instance of the minority class. 

What is the AUC metric ?
The area under the ROC curve gives a value between 0 and 1 which indicates the extent to which the model is able to separate the classes i.e to distinguish one class from the other. It is used in binary classification problems. It is represented by a chart of the TPR (y-axis) vs. FPR (x-axis) for every possible value of the threshold which determines the class to which an instance belongs. Note threshold is usually a default value of 0.5, meaning if the model returns a probability above 0.5 then the instance belongs to class 1 otherwise it is class 0.   

