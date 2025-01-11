
**INTRODUCTION**

Loan approval is one of the most important decisions financial institutions make, as it directly impacts both their profitability and how well they manage risk. To make these decisions, lenders look closely at a mix of applicant details—like their personal characteristics, creditworthiness, and loan-related factors—to determine the likelihood of repayment. Gaining insights into what influences loan approval not only helps minimize the risk of defaults but also ensures fair and efficient access to credit.
The Loan Approval Classification Dataset is a synthetic dataset designed to resemble real-world credit risk data. It includes a variety of key factors that typically influence loan approval outcomes, such as demographic information (like age, education level, and income), financial indicators (like credit scores and employment experience), and loan-specific details (like the loan amount and interest rate). With both categorical and continuous variables, the dataset offers a well-rounded foundation for exploring and predicting loan approval decisions.In previous studies, researchers have often focused on understanding how factors like credit history, income stability, or debt-to-income ratios impact a borrower’s approval chances. The advantage of using this enriched synthetic dataset is that it allows for deeper exploration of these relationships while avoiding privacy concerns tied to real financial data.


**THE DATA**

The dataset comprises 13 variables and over 45,000 observations, offering a comprehensive view of applicant profiles through key demographic, financial, and loan-related details. The demographic variables include age, gender, education level, and home ownership status, providing insight into the personal background of applicants. The financial variables capture critical indicators such as annual income, credit score, and years of employment experience, reflecting the applicant’s financial stability and creditworthiness. Finally, the loan-related details encompass the requested loan amount, interest rate, percentage of income allocated to loans, the purpose of the loan (loan intent), and the loan approval status, which serves as the target variable. Together, these features create a robust foundation for analyzing patterns and building predictive models to determine loan approval outcomes.

![CleanShot 2025-01-10 at 20 28 41@2x](https://github.com/user-attachments/assets/23db4d6a-ce96-480d-a56e-3c86ee20aafc)







        
Boxplot Distribution of all the continuous variable



**DENSITY ESTIMATION:**

Density estimation helps us understand the distribution of numerical variables and identify patterns such as skewness, peaks, or outliers in the data. By plotting the density curves for key numerical features, we can assess their spread and concentration across different ranges. This analysis provides insights into the underlying distribution of variables like income, loan amount, interest rate, and credit score, which are critical for understanding applicant characteristics and financial behaviors. The density plots allow us to visually observe how these variables are distributed and whether they exhibit any notable trends or irregularities, aiding in further analysis and model development. 


**ANALYSIS OF THE VARIABLE**

The distribution of person income is heavily right skewed, with a large portion of values concentrated near the lower range. A small number of extreme outliers exist on the higher end, pulling the tail to the right. This indicates that most individuals have relatively low incomes, as seen by the high density at the lower end of the x-axis.

<img width="220" alt="image" src="https://github.com/user-attachments/assets/b56e148e-e58f-4cd4-81e8-7bdcc97e3357" />



The loan interest rate distribution is unimodal with a noticeable right skew, meaning the tail extends towards higher values. While most loans cluster around the peak interest rate, there are some loans with significantly higher rates.

<img width="223" alt="image" src="https://github.com/user-attachments/assets/608a9584-9621-42da-ad8f-c0c9165d7f2a" />



The distribution of loan percent income is slightly right skewed, with most values concentrated at the lower end. The peak indicates that many individuals allocate a relatively small fraction of their income to loan repayments. However, the long tail on the right highlights that a smaller group of individuals allocate a much larger percentage of their income to loans.

<img width="204" alt="image" src="https://github.com/user-attachments/assets/ba78e160-7ad9-4b62-b860-4387e195dc16" />



The credit score distribution is approximately normal, showing no significant skewness.

<img width="208" alt="image" src="https://github.com/user-attachments/assets/0372d733-c52c-4727-948e-c829f84641eb" />


The loan amount distribution is multi-modal, with notable peaks around specific values like $10,000 and $20,000. This suggests that these loan amounts are particularly common, possibly reflecting standard loan thresholds or borrowing habits

<img width="205" alt="image" src="https://github.com/user-attachments/assets/a3cbc6c1-167b-499a-8124-f97dadee2666" />



The majority of cb person cred hist length values are concentrated at the lower end (between 0-10 years), indicating that most individuals have shorter credit histories. The tail extends to the right, capturing a few individuals with significantly longer credit histories (over 20 years).

<img width="233" alt="image" src="https://github.com/user-attachments/assets/c34c8292-04ae-409a-90bf-e59bad96c001" />


**NON-PARAMETRIC SMOOTHING:**

Nonparametric smoothing is a statistical technique used to estimate the underlying trend or structure of data without assuming a specific parametric form for the relationship between variables.

The plot suggests a weak, non-linear relationship between income and loan interest rates.

<img width="232" alt="image" src="https://github.com/user-attachments/assets/e7d14475-dd30-4eff-9662-9736f04f933d" />


Credit scores have minimal direct influence on loan interest rates in this dataset.

<img width="260" alt="image" src="https://github.com/user-attachments/assets/2679e299-d01a-491e-9bc9-60039a9a0e3d" />

 

**EXPLORATORY DATA ANALYSIS**

Exploratory Data Analysis  is a crucial step in understanding and preparing data for analysis. It involves summarizing key characteristics, identifying patterns, and addressing potential issues within the dataset. After cleaning the data by removing outliers, handling missing values, I used density plots to examine the data's distribution. To address skewness, I applied log transformations, ensuring the data was  evenly distributed, and standardized the variables for consistency. Following this, I delved deeper into exploring the characteristics, relationships, and patterns within the data, gaining insights that provided a strong foundation for further analysis.


 <img width="246" alt="image" src="https://github.com/user-attachments/assets/09bdc66d-c6ef-425e-af19-c665ba3f19fc" />

People in the age group 20 -25 are the group with most loans request and the main intent across that group is education and for the rest of the age group their main loan intent is medical.


<img width="248" alt="image" src="https://github.com/user-attachments/assets/2ea1ea7c-60d8-460a-8a70-e82c145a4a0b" />

The odds ratio chart reveals that venture loans have the highest odds of default compared to the baseline category (education loans). While education loans are the most common, they have relatively moderate default odds. Conversely, debt consolidation loans show the lowest odds of default, indicating that borrowers in this category are less likely to default than those in other groups. This insight suggests that loan intent is a significant factor influencing default risk, with venture loans requiring closer scrutiny.


<img width="220" alt="image" src="https://github.com/user-attachments/assets/49716533-3792-4f2e-9841-613c091313eb" />

<img width="248" alt="image" src="https://github.com/user-attachments/assets/e46c2d83-f9c9-41c1-ae88-4a1365000701" />

There is a statistically significant, positive relationship between income and loan amount, where higher incomes are associated with higher loan amounts.


<img width="244" alt="image" src="https://github.com/user-attachments/assets/5a459810-bcb6-45b9-bbeb-9a28bca26d98" />

Borrowers with personal loans have the highest average credit score (637.8), indicating better creditworthiness, while those with medical loans have the lowest (618.8), reflecting potentially greater financial vulnerability.


<img width="233" alt="image" src="https://github.com/user-attachments/assets/5cf69261-8db8-4f3e-a779-3672cd6ae31c" />

Even though most of the customers had loan related to education , education loan has the least average interest rate.



**ANOVA TEST** 

ANOVA can be a valuable tool for understanding how different categorical variables, such as loan intent , previous defaults on file or home ownership impact continuous variables like loan amount and loan interest rates. By performing ANOVA, we can assess whether there are statistically significant differences in the mean values of the continuous variables across the various categories.

Q.1) Does the loan intent effect the loan interest rate?

The analysis reveals that Loan Intent significantly influences the interest rate. However, Tukey's HSD test identified specific pairwise differences, particularly among categories like home improvement, education, and venture.

<img width="241" alt="image" src="https://github.com/user-attachments/assets/76933e4b-ceb5-41ef-81b8-d6fe4a1e9194" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/7e67bbed-1d4c-432f-bb09-a019c0169fdf" />


Q.2) Does Loan intent and previous defaults on file impact the loan interest rate?

Loan intent and borrower history significantly influence interest rates. Higher rates are charged for riskier loan purposes (e.g., medical) and borrowers with prior defaults.

<img width="235" alt="image" src="https://github.com/user-attachments/assets/274e3291-97de-437a-a7df-41ed782e7310" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/b6d1d39d-22d3-4b95-a794-e2be7656f128" />


Q.3) Does Loan intent and home ownership have an effect on the loan amount?

Both loan intent and home ownership status independently have strong effects on the loan amount. There is also a significant interaction effect, meaning that the relationship between loan intent and loan amount changes depending on home ownership status.

<img width="228" alt="image" src="https://github.com/user-attachments/assets/ce7ae7ec-d412-4c2c-be33-6f0edf93b089" />

<img width="496" alt="image" src="https://github.com/user-attachments/assets/6b02c836-8d9e-4a3a-96f1-3d041b532a46" />



**LOGISTIC REGRESSION**

Logistic regression is a statistical method used to model the probability of a binary outcome based on one or more predictor variables. For the loan dataset, it was employed to predict whether a loan would be approved or denied by analyzing key factors such as borrower income, loan characteristics, and credit history.
To build an optimal model, I began by selecting relevant variables informed by prior analyses. A correlation matrix was then examined to identify pairs of columns with a correlation coefficient above 0.5, which indicated high multicollinearity. In such cases, only one representative variable from each correlated pair was retained to reduce redundancy and improve model interpretability, ensuring that the remaining predictors provided distinct and meaningful contributions to the analysis.

<img width="467" alt="image" src="https://github.com/user-attachments/assets/ac34d3f4-85b2-4df2-92df-6f32acce33a6" />

 
After removing redundant variables, I applied stepwise selection to further refine the model by minimizing the AIC score. Multicollinearity was additionally addressed using VIF tests, confirming that the selected predictors were independent and robust. Through several iterations, the final model was refined to include key predictors such as person income, person home ownership, loan percent income, loan intent, loan int rate, credit score, and previous loan defaults on file.

<img width="349" alt="image" src="https://github.com/user-attachments/assets/f1af451d-48a3-4c9a-a7b0-a63ace374cd4" />


**ANALYSIS BASED ON THE MODEL:**

_1.	Person Income :_  There is statistically significant negative relationship between personal income and loan approval which seems pretty unexpected, as higher incomes are generally associated with an increased likelihood of loan approval due to better financial stability. A potential explanation could be that higher-income individuals tend to apply for larger loan amounts. This aligns with findings from the exploratory data analysis, which revealed a statistically significant positive linear relationship between income and loan amount. This suggests that factors like loan size or other financial variables may be influencing the observed trend.

_2.	Person home ownership :_ The fact that homeownership (OWN) has a statistically significant association with a lower likelihood of loan approval is unexpected. Generally, owning a home is seen as a positive indicator of financial stability, and homeownership is often used as a collateral advantage. 

_3.	Loan percent income :_ The statistically significant positive coefficient for loan percent income indicates that as the loan percentage of an individual’s income increases, the likelihood of loan approval also increases. This could indicate that larger loans are approved to high-need applicants despite the higher percentage of income.

_4.	Loan intent :_ The loan approval process shows statistically significant negative relationships with loan purposes such as education, medical, personal, and venture, indicating that loans for these purposes are less likely to be approved.

_5.	Loan int rate :_ A statistically significant positive relationship between interest rate and loan approval is quite interesting. Typically, one would expect higher interest rates to be charged to higher-risk applicants, meaning that a higher interest rate might indicate a higher likelihood of loan rejection. However, in this case, the significant positive coefficient suggests that higher interest rates might be used as an indicator of loan approval. This result implies that interest rate is being treated as a marker of loan acceptance, potentially reflecting the lender’s willingness to approve riskier loans at higher rates.

_6.	Credit Score :_ The statistically significant negative relationship between credit score and loan approval also seems odd. Typically, a higher credit score should increase the chances of loan approval because it reflects better creditworthiness.

_7.	Previous Loan Defaults on file :_ The previous loan defaults variable having no significant effect on loan approval is another surprising result. Normally, a history of defaults would strongly reduce the likelihood of loan approval. It's possible that the dataset doesn't accurately capture the impact of loan defaults. 




**CONFUSION MATRIX:**

The confusion matrix results show that the model demonstrated a high predictive accuracy  of 89.79%, meaning it correctly predicted almost 90% of the cases.

 
<img width="209" alt="image" src="https://github.com/user-attachments/assets/b5fd9978-92ad-4d5c-8616-ea8d3943998e" />


**ROC Curve**

<img width="239" alt="image" src="https://github.com/user-attachments/assets/50c51635-da08-4504-84b5-dac345c9f1e3" />


**AUC Value**

Area Under the Curve (AUC): 0.9550122 



**FUTURE EXPLORATION:**

While the logistic regression model aligns well with the dataset, some results, particularly the counterintuitive approval coefficients, raise concerns about real-world financial scenarios. This suggests the possibility of a lurking variable—a key factor missing from the dataset—that might better explain loan approvals. Identifying and including such variables in future iterations could significantly improve the model's interpretability and accuracy.

The confusion matrix and performance metrics further highlight areas for improvement. Despite high overall accuracy (89.79%) and sensitivity (93.68%), the model's lower specificity (76.19%) indicates difficulty in correctly identifying approved loans (class "1"), potentially due to class imbalance. Addressing this issue could involve trying alternative algorithms, such as Random Forest or XGBoost, which might better capture complex patterns. Additionally, hyperparameter tuning, adding more relevant features, and performing cross-validation could enhance the model’s robustness. Exploring external data sources or domain-specific variables to capture the influence of lurking factors could also lead to a more comprehensive and realistic model.

