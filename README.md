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
 
 The target variable is imbalanced, the data entries for attrition is around 1/6th of the total entries.
 
 <img src = "https://user-images.githubusercontent.com/105280450/209526353-a5e1556c-f10f-4b1b-a12c-f83fb6d895c5.png" height = 350 >
 
 The EDA process is further divided into univariate and bivariate analysis.
 
 1. Univariate Analysis 

    * 
 
 

    
 
