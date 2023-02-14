# Project Name - Employee Attrition Analytics and Prediction

* This is a fictional dataset created by the data scientists at IBM. It consists of parameters that could help in understanding the reasons behind an employee's decision to leave their current organization, and can also be applied to prevent futher attrition.

* Steps involved in this project-
    - Exploratory Data Analysis 
    - Data Cleaning and Transformation
    - Model Building
    - Hyper-parameter Tuning
    - Evaluation of the models

## Dataset Description

* There are 1470 records in the dataset. The target variable is the Attrition column which has two unique values- Yes and No. There are no null values.
* This dataset can be found on Kaggle via this link ---> https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset

* The input features have been divided into two types- categorical and numeric.
* Some of the features have been dropped as their description was unavailable.

* Categorical Features-
1. Business Travel- for work if the employee travels frequently, rarely or doesn't travel at all.
2. Department - the department to which the employee belongs.
3. Education - the level of education of each employee. 
    
    1. 'Below College'
    2. 'College'
    3. 'Bachelor'
    4. 'Master'
    5. 'Doctor'
 
 4. Education Field - Area of education.
 5. Environment Satisfaction - the level of work environment satisfaction.
 
    1. 'Low'
    2. 'Medium'
    3. 'High'
    4. 'Very High'
 
 6. Gender - Male or Female
 7. Job Role
 8. Job Satisfaction- the level of employees' satisfaction with their job.
 
    1. 'Low'
    2. 'Medium'
    3. 'High'
    4. 'Very High'
 
 9. Marital Status - Employee's marital status: Single,married, divorced
 10. Over18 - if the employee's age is above 18.
 11. Overtime- if the employee works overtime.
 12. Performance Rating - performance level of an employee.
 
     1. 'Low'
     2. 'Good'
     3. 'Excellent'
     4. 'Outstanding'
  
  13. Relationship Satisfaction-
  
      1. 'Low'
      2. 'Medium'
      3. 'High'
      4. 'Very High'
   
  14. Worklife Balance - 
  
      1. 'Bad'
      2. 'Good'
      3. 'Better'
      4. 'Best'
   
   * Numeric Features -
   1. Age - age of the employee.
   2. Distance from home- how far the employee lives from office.
   3. Monthly Income - monthly income of an employee.
   4. Number of Companies Worked 
   5. Total Working Years - total number of years worked in the company.
   6. Years at company- total number of years worked at the company.
   7. Years in current role - total number of years working in current role.
   8. Years since last promotion - number of years since last promotion.
   9. Years with current manager - number of years worked with current manager.
   10. Training times last year - number of trainings received in the previous year.
   11. Percent Salary Hike - % increase in salary
   
 ## Exploratory Data Analysis (EDA)
 
Here are some insights from the dataset-
 
 * The target variable is imbalanced, the data entries for attrition is around 1/6th of the total entries.
 
    <img src = "https://user-images.githubusercontent.com/105280450/209526353-a5e1556c-f10f-4b1b-a12c-f83fb6d895c5.png" height = 350 >
 
 * Univariate analysis of numeric features-
 
    ![index](https://user-images.githubusercontent.com/105280450/209543546-334574af-43d3-4b14-ae2f-579aec6d0224.png)

   #### 1. The monthly income of the employees is heavily concentrated towards the left of the distribution (peak at $2500).
   #### 2. Maximum number of employees have worked in the organization between 1 to 10 years.
   #### 3. Most employees live close to work.
   #### 4. Most employees have received a salary hike between 11% and 15%.
   
 
* Univariate analysis of categorical features -

    * Maximum number of employees have graduated with a Bachelor's or Master's degree. Many of them specialized in Life Sciences and Medical fields.
    
    <img src = "https://user-images.githubusercontent.com/105280450/209544608-92fba130-64ca-46ef-ae0e-493feda7e0b3.png" height =350>   <img src = "https://user-images.githubusercontent.com/105280450/209544787-dec7726b-f344-44f1-98e1-99beaa8745ed.png" height =350 width =400>
    
    * Most employees are happy with their work environment and are satisfied with their job.

    <img src = "https://user-images.githubusercontent.com/105280450/209545171-dedbc88a-9035-4e38-89a6-a22f3a3a4cf0.png" height =350>  <img src = "https://user-images.githubusercontent.com/105280450/209545445-97c9cabd-97af-44f0-999e-f6f95b8fde8e.png" height=350>

   
    * Around 2/5th of the employees have worked overtime and most employees have a stable work life balance.
    
    <img src = "https://user-images.githubusercontent.com/105280450/209545711-b12d9a99-252c-45e5-bfe6-6eca17222d70.png" height =350> <img src = "https://user-images.githubusercontent.com/105280450/209545764-c2008456-2d69-4ab9-9720-680d8cf08fba.png" height =350>


* Bivariate Analysis of numeric features -
  
  <img src = "https://user-images.githubusercontent.com/105280450/209546515-d6ba2a82-41c3-4c17-b457-0232420c9d6a.png" >
    
  #### 1. There is a correlation between monthly income and attrition rate; employees with lower incomes are the ones contributing to the attrition.
  #### 2. In addition, it can be inferred that employees with a higher number of work experience have continued to stay with the organization.
  #### 3. Similarly, most employees who have worked for 3 years or more with the organization are still working there.
  #### 4. Factors such as travel distance, salary hike, and number of years since last promotion do not provide much inference as the distrubutions are almost the same for both groups.
  
## Data Cleaning and Transformation

   * Some of the input features were redundant and hence were dropped from the dataset. 
   * To avoid data leakage, the dataset was divided into train,validation and test sets (60-20-20 split).
   * Categorical features were encoded to numeric form using encoding techniques such as one hot encoder.
   * As the target variable is not balanced, a combination of oversampling and undersampling was applied on the train set.

## Model Building and Hyperparamter Tuning

   * Three classification models were applied- Logistic Regression, K-nearest neighbors(KNN) classifier and Random Forest classifier.
   * Logistic Regression and Random Forest classifier models almost gave perfect predictions on train and validation sets. KNN classifier performed moderately on validation set.

## Evaluation and Performance

   * After tuning the models, Logistic Regression and Random Forest Classifier predicted with a 100% accuracy on the test set.
   * Both the above mentioned models performed well for both the classes.
   * KNN classifier gave an accuracy of around 62% on test set.
   * The precision and recall scores for Attrition = NO are higher than Attrition = YES even after balancing the target variable on running KNN model on test set.
   
   #### Model Performance on Test set -
    
   |   Model             | Best Parameter                                      | Accuracy Score   | f1 score |
   |   :----:            |    :----:                                           |     :----:    | :----: | 
   | Logistic Regression | 'C': 100, 'penalty': 'l1', 'solver': 'liblinear'    | 1.0           | 1.0 |
   | KNN classifier      |  'algorithm': 'auto', 'leaf_size': 10, 'metric': 'minkowski', 'n_neighbors': 3, 'p': 1, 'weights': 'distance'| 0.62 | No - 0.75, Yes- 0.21 |
   | Random Forest Classifier | 'bootstrap': True, 'max_depth': 10, 'min_samples_leaf': 3, 'min_samples_split': 8, 'n_estimators': 100| 1.0 | 1.0 |


## Conclusion 
   
   * Although Logistic Regression and Random Forest Classifier produced accurate results on the test set, the same results may not be obtained for new data records.
   * As the dataset consists of around 1500 records, these results might not explain for the entire population.
   * In addition, due to the class imbalance problem the target variable was undersampled and oversampled which basically produced duplicate records in the dataset. Hence, the train, validation and test sets may share the same distribution, thus, giving 100% accuracy.
   * Another possible reason could be the luck factor when the data was sampled and shuffled for the first time. For this sample, the models might have performed well but for another sample the same may not be the case.
   * More data is required to make accurate predictions.

