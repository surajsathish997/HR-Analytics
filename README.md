
**Introduction **
The HR Employee Attrition dataset provides valuable insights into employee turnover within organizations. Employee attrition is a critical concern for businesses as it can have significant impacts on productivity, morale, and overall organizational success. Understanding the factors contributing to employee attrition and developing effective strategies to mitigate it is essential for maintaining a stable and engaged workforce. 
The primary objective of this analysis is to identify key factors influencing employee attrition and build a predictive model to forecast attrition risk. By exploring the dataset and applying data analysis techniques, we aim to uncover patterns, relationships, and insights that can help us better understand the drivers of attrition. The goal is to provide actionable recommendations to HR professionals and decision-makers to proactively address employee attrition and improve retention strategies.
Our analysis will focus on achieving the following goals and objectives:
-	Identify the most significant factors associated with employee attrition, such as job satisfaction, work-life balance, and career development opportunities.
-	Assess the influence of demographic variables, including age, gender, and education, on attrition rates.
-	Explore the relationships between job-related characteristics, such as job role, department, salary, and attrition.
-	Develop a predictive model to forecast employee attrition and evaluate its performance in terms of accuracy and predictive power.
-	Provide actionable insights and recommendations to HR professionals and decision-makers for implementing effective employee retention strategies.
This technical report is intended for HR professionals, managers, and decision-makers within the organization who are responsible for employee retention and workforce management. The findings and recommendations presented in this report aim to guide strategic decision-making and inform the development of targeted interventions to address attrition challenges. Additionally, individuals interested in human resources and employee attrition research will also find value in this report.

**Data Dictionary**
Column Name	Description
Age	The age of the employee (numeric)
AttritionBoolean	Attrition status of the employee (0 - No, 1 - Yes)
Attrition	Attrition status of the employee (Yes or No)
BusinessTravel	Frequency of business travel (Non-Travel, Travel Rarely, Travel Frequently)
DailyRate	The daily rate of pay for the employee (numeric)
Department	The department in which the employee works (e.g., Sales, Research & Development, Human Resources)
DistanceFromHome	Distance from employee's home to workplace (numeric)
Education	Employee's level of education (1 - Below College, 2 - College, 3 - Bachelor, 4 - Master, 5 - Doctor)
EducationField	Field of study of the employee (e.g., Life Sciences, Medical, Marketing, Technical Degree)
EnvironmentSatisfaction	Employee's satisfaction with the work environment (1 - Low, 2 - Medium, 3 - High, 4 - Very High)
Gender	Employee's gender (Male or Female)
HourlyRate	Hourly rate of pay for the employee (numeric)
JobInvolvement	Employee's level of job involvement (1 - Low, 2 - Medium, 3 - High, 4 - Very High)
JobLevel	Job level of the employee (1 - Entry Level, 2 - Intermediate, 3 - Senior, 4 - Manager, 5 - Director)
JobRole	Role/title of the employee (e.g., Sales Executive, Research Scientist, Laboratory Technician)
JobSatisfaction	Employee's job satisfaction level (1 - Low, 2 - Medium, 3 - High, 4 - Very High)
MaritalStatus	Employee's marital status (Single, Married, Divorced)
MonthlyIncome	Monthly income of the employee (numeric)
MonthlyRate	Monthly rate of pay for the employee (numeric)
NumCompaniesWorked	Number of companies the employee has worked for (numeric)
Over18	Age of the employee is over 18 years (Yes or No)
OverTime	Whether the employee works overtime or not (Yes or No)
PercentSalaryHike	Percentage increase in salary (numeric)
PerformanceRating	Employee's performance rating (1 - Low, 2 - Good, 3 - Excellent, 4 - Outstanding)
RelationshipSatisfaction	Employee's satisfaction with their relationships at work (1 - Low, 2 - Medium, 3 - High, 4 - Very High)
StockOptionLevel	Employee's level of stock option grants (0 - None, 1 - Low, 2 - Medium, 3 - High)
TotalWorkingYears	Total number of years the employee has worked (numeric)
TrainingTimesLastYear	Number of training sessions attended by the employee in the last year (numeric)
WorkLifeBalance	Employee's perceived work-life balance (1 - Bad, 2 - Good, 3 - Better, 4 - Best)
YearsAtCompany	Number of years the employee has been with the company (numeric)

**Data Cleaning**
Add an extra column for Attrition to make it 1 and 0.
Delete EmployeeCount column as it’s a static column with a value of 1 and doesn’t add anything to analysis.
Delete StandardHours column as it’s a static column with a value of 80 and doesn’t add anything to analysis.
 
**Dataset **
The dataset contains a total of 1470 observations and 33 features (Figure 1.0). Some of the key features include age, department, education level, job satisfaction, and marital status. The target variable, ‘AttritionBoolean’ indicates whether an employee has left the organization (1) or is still employed (0). These features provide a comprehensive view of the employees and allow for in-depth analysis of the factors that may include attrition.
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/4c939b5a-d6ef-449b-9fcd-066f8fda9a2c)
Figure 1.0
The dataset contains a mix of categorical and numerical features (Figure 1.1). Categorical features, such as gender and department, provide information about employee characteristics, while numerical features, such as age and job satisfaction, offer quantitative measurements. The combination of feature types enables a holistic analysis of the dataset, considering both qualitative and quantitative factors.
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/4fefb1e5-e4da-4b9d-ba16-1e46e6e1da05)
Figure 1.1
No nulls were found in the dataset (Figure 1.2). This indicates that the dataset is complete and does not have any missing information for the provided features. The absence of null values ensures the integrity of the dataset and allows for a more accurate analysis and modelling.
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/b54bda1d-cb6e-48f5-b47d-2f4e855097e3)
Figure 1.2
 
**Patterns, Trends, and Insights**
In the dataset, there are 237 instances where employees have been attrited (Figure 1.3), indicating that they have left the organization. On the other hand, there are 1233 instances where employees have not been attrited, indicating that they have chosen to remain with the organization.
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/2f300084-8d5b-4ec3-bbf9-c1d917c5eb0d)
Figure 1.3
The distribution of age in the dataset exhibits a wide range, spanning 18 to 60 years (Figure 1.4). The majority of employees fall within the age range of late 20’s to early 40’s, indicating a relatively diverse age demographic within the organization.
Upon analysing the attrition status in relation to age, it becomes apparent that attrition rates are highest among employees between 25-35, gradually decreasing as age increases. This observation suggests that younger employees, particularly those in their late 20’s and early 30’s, may be more likely to leave the organization compared to their older counterparts.
One possible explanation for this pattern could be that younger employees are more inclined to explore opportunities and career advancements. They may be seeking growth prospects or better work-life balance elsewhere. On the other hand, older employees who have been with the organization for a longer duration might have developed a sense of loyalty or stability, and thus are less prone to attrition.
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/ca4e18ef-10cc-4745-ba09-97afbce1d968)
Figure 1.4: Age compared with Attrition
The earlier analysis has prompted a look at work life balance and seeing if there are any trends between attrition and an employees’ work life balance. When analysing the relationship between work-life balance and attrition using a violin plot (Figure 1.5), we observe distinct patterns across different age brackets. The work-life balance categories are represented by numerical values, where 1 corresponds to ‘Bad’, 2 to ‘Good’, 3 to ‘Better’, and 4 to ‘Best’. 
For the 18-30-year age group, non-attrited employees mostly perceive their work-life balance as 'Better' (3), indicating a satisfactory balance between work and personal life. However, attrited employees in the same age group tend to rate their work-life balance as 'Good' (2) more frequently. This suggests that attrited employees may have experienced some dissatisfaction or imbalance in their work-life dynamics.
Similarly, in the 30-40-year age group, non-attrited employees report a significant proportion of 'Better' (3) work-life balance ratings. However, attrited employees in this age group exhibit a pattern similar to the 18-30 year age group, with higher occurrences of 'Good' (2) ratings.
These findings emphasize the importance of addressing work-life balance concerns within the organization. The observed trend of attrited employees perceiving their work-life balance as suboptimal suggests that improvements in this area could contribute to better employee retention and satisfaction. 
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/c7b72b83-f9d9-4728-9479-bd4b47d763e3)
Figure 1.5 : Work-Life Balance compared with Attrition
A correlation matrix (Figure 1.6) was examined to gain insights into the relationship between attrition and other features. The correlation matrix provides a comprehensive overview of the associations between attrition and various factors within the dataset.  
Upon analysing the correlation matrix, it is evident that many of the correlations between attrition and other features skew towards the negative side. This indicates a general tendency for these features to have an inverse relationship with attrition. However, it is important to note that the observed correlations are relatively weak, with the negative coefficients only slightly under 0. Some of the strongest negative correlations are observed between attrition and job level (-0.17), attrition and age (-0.16), and attrition and years with current manager. These findings suggest that as job level, age, years, in current role, and years with the current manager increase, the likelihood of attrition decreases slightly. It is important to exercise caution when interpreting these correlations, as correlation does not always imply causation.
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/159bdfed-a8e0-41b5-a3be-60b329202b4e)
Figure 1.6 : Correlation Matrix
The graphs below (Figure 1.7) further explores the correlation between certain variables and attrition:
•	Department vs Attrition: The p-value of 0.005 suggests a significant association between department and attrition. This indicates that the department in which an employee works may have an impact on their likelihood of attrition.
•	Education vs Attrition: The p-value of 0.546 indicates that there is no strong evidence of an association between education level and attrition. Therefore, education level may not play a significant role in determining attrition.
•	Gender vs Attrition: With a p-value of 0.291, there is no strong evidence to suggest a significant association between gender and attrition. Gender may not be a major contributing factor to attrition in the given dataset.
•	JobLevel vs AttritionBoolean: The p-value of 0.000 indicates a highly significant association between job level and attrition. This suggests that employees at different job levels may have varying levels of attrition, with lower job levels potentially experiencing higher attrition rates.
•	JobSatisfaction vs Attrition: The p-value of 0.001 indicates a significant association between job satisfaction and attrition. Employees with different levels of job satisfaction may exhibit different attrition patterns, with lower job satisfaction potentially contributing to higher attrition rates.
•	MaritalStatus vs Attrition: With a p-value of 0.000, there is strong evidence of an association between marital status and attrition. Marital status may play a role in determining attrition, with different marital statuses exhibiting different attrition rates.
In summary, the analysis highlights that department, job level, job satisfaction, and marital status are factors that show a significant association with attrition in the given dataset. Understanding and addressing these factors could be crucial for managing attrition and improving employee retention within the organization. However, education level and gender do not appear to have a strong influence on attrition based on the analyzed data.
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/ac4a09c7-5205-4e51-ac7a-b4f017809c15)
Figure 1.7 : p-value analysis

**Prediction Models**
In order to predict employee attrition, three different models were evaluated: K-nearest neighbors (KNN), Logistic Regression, and Random Forest. The following features were considered based on their p-value analysis (Figure 1.7): 'Age', 'Department', 'JobLevel', 'JobSatisfaction', and 'MaritalStatus'. Each model was assessed based on its accuracy in predicting employee attrition.
The baseline accuracy, which represents the accuracy of a simple model that always predicts the majority class, was found to be 0.8388.
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/ad6e04a4-7a2c-4eda-9ce2-d2d6edf2ce16)
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/8b787aa7-e888-46ff-8ea2-c6327cd2b97c)
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/15f51572-4f54-4a5c-becf-8811f5d51f10)
K-nearest neighbors (KNN):
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/3ff393e3-1db5-4148-abaf-d7b05863c3d6)
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/dbc1bbb6-bf64-4c3c-854b-389b205a43dd)
Logistic Regression:
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/ee46bef9-5469-4d73-baf2-b5e8f58dd4d6)
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/1e7b1b39-127b-4c29-9a7d-3cf329b5f263)
Random Forest:
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/552ff8a2-4576-4e46-9860-6ec7a0326219)
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/238a3847-fca4-44ca-a152-02a17b984714)
![image](https://github.com/surajsathish997/HR-Attrition-Analysis/assets/18410759/7b0fe4f3-16e4-44fd-88f1-498d6a67a28a)

**Summary:**
Among the models evaluated, Logistic Regression yielded the highest accuracies, ranging from 0.8408 to 0.8429. This indicates that the Logistic Regression model outperformed the baseline accuracy, demonstrating its effectiveness in predicting employee attrition.
Therefore, based on the analysis, the Logistic Regression model utilizing the features 'Age', 'Department', 'JobLevel', 'JobSatisfaction', and 'MaritalStatus' is recommended for predicting employee attrition.



**Recommendations**
Attrition can have significant negative impacts on an organization, including loss of talent, decreased productivity, and increased recruitment costs. This section provides recommendations based on the analysis of the key features that were identified which influenced attrition. These key features were age, department, job level, job satisfaction, and work-life balance. 
Work-Life Balance: It is evident that work-life balance plays a crucial role in employee satisfaction and attrition rates. Based on the analysis, it was revealed that employees in certain age groups are more susceptible to attrition. By providing flexible work hours, remote work options, or other benefits the organization can address specific needs of certain employee groups. Employees who perceive a lack of work-life balance are more likely to experience job dissatisfaction and consider leaving the organization.
Career Development and Growth: Younger employees showed higher attrition rates, indicating a potential desire for growth and advancement. To address this, the organization should provide ample opportunities for career development, growth, and advancement. Implement mentorship programs, training initiatives, and clearly defined career paths to engage and retain young talent, fostering a sense of progression and achievement.
Enhance Job Satisfaction: Job satisfaction emerged as a significant factor associated with attrition. To improve job satisfaction, the organization should create a positive work environment that promotes open communication, recognition of employee achievements, and opportunities for professional development. By addressing employee concerns and fostering a satisfying work atmosphere, attrition rates can be reduced.
Implementation of these recommendations, accompanied by regular monitoring and evaluation of attrition rates and employee satisfaction levels, will provide valuable insights for ongoing improvements in attrition management strategies. By proactively addressing attrition concerns, the organization can enhance employee retention, productivity, and overall organizational success.
