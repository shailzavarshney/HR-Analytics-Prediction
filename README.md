# HR Analytics Prediction: Why Do People Resign?

This project focuses on analyzing employee churn in an organization to identify the factors contributing to attrition and develop a predictive model that helps businesses retain their employees.

## **The Importance of Churn Prediction in Organizations**
Employee churn is a critical issue for organizations, as it directly impacts productivity, operational costs, and overall business performance. Below are some key statistics highlighting the challenges:
- **Hiring and Retention Challenges**: Small business owners spend 40% of their working hours on non-revenue-generating tasks like hiring.
- **Financial Impacts of Churn**: An average company loses between 1% and 2.5% of their total revenue during the time it takes to onboard and train a new hire.
- **Time to Fill a Position**: It takes 52 days on average to fill a vacant position, causing disruptions in productivity.

By proactively identifying employees at risk of leaving, organizations can implement retention strategies, reduce hiring costs, and improve overall workforce stability.

## **Data Source**
The dataset used for this project is available on Kaggle:  
[IBM HR Analytics Attrition Dataset](https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset)

## **Dataset Description**
The dataset contains **1,470 observations** and **35 features**. Key features include:
- **Age**: Age of the employee.
- **BusinessTravel**: Frequency of business travel.
- **DailyRate**: Daily income of the employee.
- **Department**: Department the employee works in.
- **DistanceFromHome**: Distance between the employee’s home and workplace.
- **Education**: Level of education (1-5 scale).
- **EducationField**: Field of education (e.g., Life Sciences, Technical, etc.).
- **EmployeeCount**: Number of employees in the organization (constant in this dataset).
- **EmployeeNumber**: Unique identifier for the employee.
- **EnvironmentSatisfaction**: Satisfaction with the work environment (1-4 scale).
- **Gender**: Gender of the employee.
- **HourlyRate**: Hourly income of the employee.
- **JobInvolvement**: Level of job involvement (1-4 scale).
- **JobLevel**: Job level (1-5 scale).
- **JobRole**: Job role (e.g., Sales Executive, Manager, etc.).
- **JobSatisfaction**: Satisfaction with the job (1-4 scale).
- **MaritalStatus**: Marital status (e.g., Single, Married, Divorced).
- **MonthlyIncome**: Monthly income of the employee.
- **MonthlyRate**: Monthly rate of pay.
- **NumCompaniesWorked**: Number of companies the employee has worked at.
- **Over18**: Whether the employee is over 18 (constant in this dataset).
- **OverTime**: Whether the employee works overtime (Yes/No).
- **PercentSalaryHike**: Percentage of salary hike.
- **PerformanceRating**: Performance rating (1-4 scale).
- **RelationshipSatisfaction**: Satisfaction with relationships at work (1-4 scale).
- **StandardHours**: Standard working hours (constant in this dataset).
- **StockOptionLevel**: Level of stock options offered (0-3 scale).
- **TotalWorkingYears**: Total years of work experience.
- **TrainingTimesLastYear**: Number of training sessions attended last year.
- **WorkLifeBalance**: Work-life balance rating (1-4 scale).
- **YearsAtCompany**: Years spent at the current company.
- **YearsInCurrentRole**: Years spent in the current role.
- **YearsSinceLastPromotion**: Years since the last promotion.
- **YearsWithCurrManager**: Years working with the current manager.

## **Hypotheses**
Below are potential hypotheses about how different factors may affect employee churn:
1. **Age**: Younger employees may have higher churn due to career exploration.
2. **BusinessTravel**: Frequent business travel may increase churn due to stress and lack of work-life balance.
3. **DailyRate & MonthlyIncome**: Lower income levels might correlate with higher churn rates.
4. **Department**: Certain departments (e.g., Sales) may experience higher churn due to job pressure.
5. **DistanceFromHome**: Employees living farther from work may be more likely to leave.
6. **Education & EducationField**: Higher education levels might correlate with lower churn due to better job satisfaction.
7. **EnvironmentSatisfaction**: Employees dissatisfied with their work environment are more likely to churn.
8. **JobSatisfaction**: Lower job satisfaction can lead to higher churn rates.
9. **MaritalStatus**: Single employees may churn more often due to fewer family constraints.
10. **OverTime**: Employees working overtime may have higher churn due to burnout.
11. **PercentSalaryHike**: Employees receiving smaller salary hikes may churn more often.
12. **PerformanceRating**: Lower-rated employees may churn due to lack of growth opportunities.
13. **WorkLifeBalance**: Poor work-life balance may significantly contribute to churn.
14. **YearsAtCompany & YearsInCurrentRole**: Employees with longer tenures may churn less due to loyalty.

## **Steps**
1. **Data Exploration**: Understanding the dataset and identifying patterns.
2. **Feature Engineering**: Creating relevant features for churn prediction.
3. **Data Preprocessing**: Handling missing values, encoding categorical data, and scaling.
4. **Model Building**: Using machine learning algorithms to predict churn.
5. **Model Evaluation**: Assessing performance using metrics like accuracy, precision, recall, and F1-score.
6. **Insights & Recommendations**: Providing actionable insights based on the analysis.

## **Summary**

### **Dataset Overview**
- **Structure**: The dataset comprises 1,470 observations (rows) and 35 features (variables).
- **Missing Data**: No missing data, which simplifies analysis and modeling.
- **Data Types**: The dataset contains only two data types: factors (categorical) and integers (numerical).
- **Target Variable**: The label, **Attrition**, indicates whether an employee left the organization. The goal is to understand the factors contributing to employee attrition.
- **Imbalanced Dataset**:
  - **1237 employees** (84%) stayed in the organization.
  - **237 employees** (16%) left, making this an imbalanced dataset.

### **Key Findings**

#### **Demographics and Attrition**
- **Age by Gender**: Both distributions are similar.
- **Job Satisfaction by Gender**: Among employees who stayed, job satisfaction levels are comparable across genders. Among employees who left, females had lower job satisfaction than males.
- **Departments**: While males dominate most departments, females are more prevalent in Research and Development.

#### **Generational Analysis**
- **Employees Who Quit**:
  - Boomers had a higher number of previous employers.
  - Millennials are still early in their careers, but their turnover rate is the highest.
- **Attrition by Generation**:
  - Millennials exhibit the highest attrition rate, likely due to career exploration.
  - Boomers’ attrition may be linked to retirement.
- **Attrition by Education**:
  - Employees with bachelor’s degrees have the highest attrition rate, correlating with millennials’ dominance in this group.

#### **Income and Job Satisfaction**
- **Income by Department**: Significant differences exist in attrition rates by department income levels.
- **Income by Job Satisfaction**: Lower job satisfaction widens the income gap between employees who leave and those who stay.
- **Attrition by Salary**:
  - Most employees who left earned less than $7,000 monthly and had salary hikes of less than 15%.

#### **Work Conditions**
- **Overtime**: Over 54% of employees who left worked overtime, potentially indicating burnout.
- **DailyRate Differences**: Healthcare Representatives, Sales Representatives, and Research Scientists show notable differences in daily rates, suggesting income disparity as a potential factor.
- **Working Environment**: Managers and Healthcare Representatives face poorer working environments, while Sales Representatives, who often work outside the office, do not experience this issue.

#### **Attrition by Job Role**
- **Job Roles with Most Employees**: Sales and Research Scientists.
- **Highest Salaries by Role**: Managers and Research Directors.
- **Highest Attrition by Role**: Sales Representatives, Healthcare Representatives. Managers, especially those recently hired, report lower satisfaction scores.

## **Key Observations**
- People tend to switch to different jobs at the start of their careers or the earlier parts of it. Once they have settled with a family or found stability, they tend to stay longer in the same organization, only seeking vertical movements.
- **Salary** and **stock options** are great motivators for employees, and those with higher pay and more stock options show greater loyalty to their company.
- **Work-life balance** is a significant motivation factor for employees. However, people with a good work-life balance tend to switch jobs in search of better opportunities and a higher standard of living.
- Departments where target meeting performance is crucial (e.g., Sales) tend to have higher chances of attrition compared to departments with more administrative roles (e.g., Human Resources).
- People with high **Job Satisfaction** and **Environment Satisfaction** are loyal to the organization. Conversely, those who are dissatisfied with their current projects tend to leave the organization more frequently.
