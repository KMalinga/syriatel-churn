### SyriaTel Customer Churn - A Machine Learning Classification Approach
### Introduction
Customer churn is a significant challenge in the telecommunications industry, driven by factors like market shifts, evolving customer preferences, and fierce competition. SyriaTel, like its counterparts, grapples with retaining customers amidst these complexities. However, data analytics and machine learning offer a promising solution.

By analyzing customer data, SyriaTel can leverage predictive modeling and segmentation to uncover churn patterns and drivers. Machine learning strengthens this process by identifying hidden correlations and accurately predicting customer behavior. With these insights, SyriaTel can implement personalized retention strategies, bolstering customer retention and achieving sustainable growth.

In essence, embracing data-driven approaches empowers SyriaTel to:

Understand churn challenges
Develop effective retention strategies
Adapt to industry changes
Ensure long-term success
Notebook Preview

Business Understanding
Data Understanding
Data Cleaning
Exploratory Data Analysis
Data Preparation
Modeling
Conclusion
### 1. Business Understanding

High customer churn rates plague SyriaTel, similar to many telecommunications companies. This results in substantial financial losses and hinders sustainable progress. Traditional churn prediction methods have proven ineffective, leading to wasted resources and unsuccessful retention efforts.

SyriaTel can overcome this challenge by harnessing advanced analytics and machine learning. By delving into historical customer data, SyriaTel can unearth patterns in behavior, preferences, and usage that signal potential churn. Equipped with this foresight, SyriaTel can craft tailored retention strategies for individual customers, significantly reducing churn rates and safeguarding revenue streams.

Proactive churn management not only addresses immediate revenue concerns but also cultivates enduring customer loyalty and strengthens SyriaTel's competitive edge. Investing in advanced analytics and machine learning goes beyond optimizing customer retention; it positions SyriaTel as an industry leader dedicated to customer satisfaction and sustained growth.

Problem Statement

Customer churn poses a significant threat to telecommunications companies like SyriaTel, despite offering competitive services. Uncovering the underlying factors driving churn and implementing effective retention strategies is crucial. Leveraging data analytics and machine learning to dissect customer data is promising, but necessitates accurate identification of churn predictors. The challenge lies in utilizing these techniques to develop proactive measures, enhance customer satisfaction, and drive sustainable business growth.

Objectives

Develop a predictive classifier for SyriaTel to identify predictable patterns of customer churn.
Determine key factors influencing customer churn within the telecommunications company.
Assess classifier performance using metrics like accuracy, precision, recall, F1-score, and confusion matrix to gauge effectiveness.
Offer actionable recommendations to SyriaTel to mitigate losses attributed to customer churn.
Metric of Success

The project will be considered successful if the classification model achieves the following:

High proportion of accurately identified churners (High Recall)
Low number of false positive predictions (Low False Positive Rate)
Good generalization performance (Accuracy of 80% on unseen dataset)
### 2. Data Understanding

The dataset, obtained from Kaggle (https://www.kaggle.com/datasets/blastchar/telco-customer-churn), comprises 3333 rows and 21 columns. All features, except phone number and state, have numerical values. The remaining features are categorical or binary (international plan, voice mail plan, and churn). The churn column (target variable) is represented as:

1 - True (Churned)
0 - False (Not Churned)
This is a binary classification problem where the goal is to predict the likelihood of a customer churning.

Table: Dataset Columns

Column Name	Description
State	Represents states in the USA
Account Length	Length of time (seconds/minutes) a customer's account has been active
Area Code	Geographic area code of a customer's phone number
Phone Number	Customer's phone number
International Plan	Indicates if a customer has an international call plan (Yes/No)
Voice Mail Plan	Indicates if a customer has a voice mail plan (Yes/No)
Number Vmail Messages	Number of voice mail messages left by a customer
Total Day Minutes	Total time (minutes) spent on daytime calls
Total Day Calls	Total number of calls made during the day
Total Day Charge	Total charge for daytime calls
Total Eve Minutes	Total time (minutes) spent on evening calls
Total Eve Calls	Total number of calls made in the evening
Total Eve Charge	Total charge for evening calls
Total Night Minutes	Total time (minutes) spent on night calls
Total Night Calls	X

drive_spreadsheet
Export to Sheets
### 3. External Dataset Validation
The telecommunications industry continues to face a significant and costly challenge in the form of customer churn. A recent research study conducted in 2018 by [Mason, A.](2018, June). Connected Consumer 2017: Mobile Customer Satisfaction and Churn in Sub-Saharan Africa [Sample]. Analysis Mason. Retrieved from https://www.analysysmason.com/globalassets/x_migrated-media/media/analysys_mason_ssa_mobile_satisfaction_sample_jun2018_rdmm03.pdf, a consulting and research company, highlights this issue. The study, titled "Connected Consumer 2017: Mobile Customer Satisfaction and Churn in Sub-Saharan Africa", was led by senior analyst Karim Yaici and research director Stephen Sale.

According to the study, the intention to churn among telecommunication subscribers in the sub-Saharan African region ranged from 9% to 16% across all operators surveyed [Mason, 2018]. This figure is in line with churn rates in other regions, but lower compared to the neighboring Middle East and Africa (MENA) region, where the intention to churn within 6 months was recorded at an average of 22% [Mason, 2018].

The study also found that customer service had a significant impact on churn for subscribers in South Africa, where the average churn rate was 17% [Mason, 2018]. This effect was much greater compared to the other countries covered, which may reflect the differences in market maturity in the region. The findings from this study serve as external validation for the importance of customer service in reducing churn in the telecommunications industry.

### 4. Modeling
The churn classification problem is tackled with approximately six algorithms, with the focus on tuning the two best performing models. Some of the algorithms used include:

Logistic Regression Classifier: This is a baseline model that finds the best line to separate the two classes in a high-dimensional space.
Adaboost: This model iteratively improves performance by focusing on data points that are difficult to classify.
Gradient Boosting: This model is known for its high accuracy and performance.
Random Forest: This model reduces overfitting, a common issue with decision trees.
Decision Tree: This is a core machine learning algorithm used for classification.
Hyperparameter Tuning: This process involves optimizing the parameters of the decision tree and random forest models to achieve better performance.
Random forest and the tuned random forest model emerged as the top performers, boasting higher prediction accuracy and superior discrimination between churned and non-churned customers. Notably, the model excelled at identifying customers who would not churn (class 0) with high precision, recall, and F1-score, while minimizing false negatives. Additionally, it maintained a low false positive rate, minimizing the number of customers erroneously flagged as likely to churn.

### 5. Conclusion
The random forest model achieved a strong accuracy of 0.95 in predicting churn rate, with a consistent performance across folds in cross-validation (k=5). Notably, the model excelled at identifying customers who would not churn (class 0) with precision, recall, and F1-score all around 0.97.

While the model performed well overall, it's important to acknowledge a slight decrease in precision, recall, and F1-score (around 0.82) for churned customers (class 1). This highlights an opportunity for further improvement in identifying customers at risk of churn.

Despite this, the random forest model remains the most effective model for predicting churn rate based on the overall accuracy and balanced performance across metrics.

### 6. Recommendation
Feature Engineering: Uncover deeper customer insights by creating new features like average daily/monthly charges or call duration. This can reveal important usage patterns that aid in predicting churn risk.
Targeted Engagement: Gather valuable feedback through customer satisfaction surveys, focusing on aspects like network coverage and service. Additionally, leverage anonymized demographic data (age, location) to tailor plans that better suit individual needs, increasing customer satisfaction and reducing churn.
Competitive Pricing: Price remains a key factor in customer retention. Offering competitive pricing and packages that deliver good value for money incentivizes customers to stay with your company rather than seek alternatives.
Loyalty Programs: Implement loyalty programs that reward long-term customers with exclusive benefits and incentives. This fosters a sense of loyalty and encourages continued engagement with your brand, ultimately reducing churn.

Repository Guide https://github.com/KMalinga/syriatel-churn
Dataset: https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download

