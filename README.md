# VisaDecisionPredictor

PROBLEM STATEMENT

United States of America is known as the land of opportunity. Every year hundreds and thousands of individuals arrive in the United States with a dream to achieve something big in their lives. One of the major problems that every individual who’s not a US citizen faces, is the strenuous process of applying for a permanent work visa. This problem is faced by the international workers as well as the international students. A permanent labor certification issued by the Department of Labor (DOL) allows an employer to hire a foreign worker to work permanently in the U.S. The employer must obtain a certified labor certification application from the DOL’s Employment and Training Administration. After this step, the employer can submit an immigration petition to the Department of Homeland Security’s U.S. Citizenship and Immigration Services (USCIS). This process depends on a lot of different factors and it can take several years before the process completes. This is a major problem which U.S. as well as international employers face today. This problem needs to be addressed carefully in order for an employer to successfully allow an employee to work for their company in the States.

To tackle this major societal problem, we will be designing several machine learning models that will help us to predict the visa decisions based on the employer, employee, wage etc. Hopefully, our models will be robust enough and will be able to predict whether a visa application will be approved or denied. This will help us to resolve one of the major societal issue that every company inside or outside of the United States faces today. 

DATASET SOURCE

For our training & testing data, we will be using the US Permanent Visa Application dataset which has been collected and distributed by the US Department of Labor. This dataset is available on Kaggle. This dataset contains a detailed information on 374k visa decisions. The data has been collected between 2012-2017 and includes information on employer, position, wage offered, job posting history, employee education, past visa history, associated lawyers and final decision. This dataset consists of 154 attributes and 374362 instances. Some of the major features of the dataset are mentioned below:
•	application_type
•	case_status (target feature)
•	class_of_admission
•	country_of_citizenship
•	employer_name
•	us_economic_sector






APPROACH

We will be implementing the following CRISP-DM approach to deal with the above-mentioned problem:
•	Firstly, we will be focusing on the business & data understanding part of the problem
•	Secondly, we will be performing data pre-processing, cleaning, wrangling & exploratory data analysis. Here, we will be taking care of all the null values present in the dataset. We will also be converting our target variable – case_status – into a binary class. For this, we will be merging ‘Certified’ and ‘Certified-Expired’ case_status into one label. Similarly, we will be merging ‘Denied’ and ‘Withdrawn’ case_status into another label. 
•	We will also be performing various feature engineering steps that will be required for our models – one-hot encoding, discretization, normalization
•	We will be performing the exploratory data analysis as well that will help us visualize different features against the target feature
•	We will be treating this problem as a binary classification problem where 0 indicates that the visa application has been approved and 1 indicates that the application has been denied
•	Thirdly, we will be implementing various machine learning algorithms including Logistic Regression, KNN, Random Forest, Gradient Boost, SVM. We will be using these data mining algorithms for our data set because we are trying to solve a binary classification problem here. All the above-mentioned algorithms will work really well in our case as we are tackling a classification problem
•	Finally, we will be evaluating our models based on an appropriate evaluation metric

EVALUATION

The problem we are trying to tackle here is to predict whether a given visa application will be approved or rejected. We have considered this as a binary classification problem. Our models will be classifying the target class – case_status - with binary class labels: 0 – ‘Visa Application Approved’; 1 – ‘Visa Application Denied’. We will be evaluating our approach on the basis of the evaluation metric – ‘Recall’. Though, ‘Accuracy’ is also a suitable measure to evaluate the performance of our models, we will be using ‘Recall’ because we need to decrease the number of ‘false-negatives’ for our classification problem. It is immensely necessary for our models to predict the case_status as ‘Denied’ when it’s actually ‘Denied’. We do not want our models to predict the case_status as ‘Approved’ when it is actually ‘Denied’ as that would defeat the overall purpose of our visa application status prediction task.
