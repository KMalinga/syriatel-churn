# SyriaTel-Customer-Churn-A-Machine-Learning-Classification-Approach

## Introduction.
Customer churn presents numerous challenges in the telecommunications industry, including market shifts, evolving preferences, and fierce competition. Syrialtel, like its counterparts, faces the task of retaining customers amidst these complexities. However, leveraging data analytics and machine learning offers a promising solution.

By analyzing customer data, Syrialtel can uncover churn patterns and drivers using predictive modeling and segmentation. Machine learning enhances this process by identifying hidden correlations and predicting customer behavior accurately. With these insights, Syrialtel can implement personalized retention strategies, increasing customer retention and fostering sustainable growth.

In summary, by embracing data-driven approaches, Syrialtel can understand churn challenges, develop effective strategies, and adapt to industry changes, ensuring long-term success.

## Notebook Preview.
1. Business Understanding
2. Data Understanding
3. Data Cleaning
4. Exploratory Data Analysis
5. Data Preparation
6. Modelling
7. Conclusion

## 1. Business Understanding
SyriaTel, like numerous telecommunications firms, grapples with the persistent challenge of high customer churn rates, which lead to significant financial setbacks and impede sustainable progress. Traditional churn prediction methods have proven futile, resulting in wasted resources and ineffective retention endeavors.

To confront this dilemma, SyriaTel can harness advanced analytics and machine learning. By delving into historical customer data, SyriaTel can unearth patterns in behavior, preferences, and usage that signal potential churn risks. Equipped with this foresight, SyriaTel can craft tailored retention strategies for individual customers, markedly diminishing churn rates and safeguarding revenue streams.

Through proactive churn management, SyriaTel not only addresses immediate revenue concerns but also cultivates enduring customer loyalty and bolsters its competitive standing in the market. Investing in advanced analytics and machine learning not only optimizes customer retention but also distinguishes SyriaTel as an industry leader devoted to customer satisfaction and sustained growth.

In essence, by leveraging advanced analytics and machine learning, SyriaTel can devise a robust churn prediction model that not only tackles immediate revenue loss but also fosters enduring customer relationships and propels sustainable business expansion.



> **Problem statement:**
 >* Customer churn poses a significant challenge for telecommunications companies like Syrialtel, despite offering competitive services. Understanding the underlying factors driving churn and implementing effective retention strategies is crucial. Leveraging data analytics and machine learning to dissect customer data is promising but requires accurate identification of churn predictors. The challenge is to utilize these techniques to develop proactive measures, enhance customer satisfaction, and drive sustainable business growth


> **Objectives**:
 >* Develop a predictive classifier for SyrialTel Telecommunication to identify predictable patterns of customer churn.
 >* Determine key factors influencing customer churn in the Telecommunication company.

>* Assess classifier performance using metrics including accuracy, precision, recall, F1 score, and confusion matrix to gauge effectiveness.

>* Offer actionable recommendations to SyrialTel to mitigate losses attributed to customer churn.

> **Metric of Success**
The project wil be considered a success if the classification model accurately identifies a high proportion of actual churners(High Recall) with a low number of false positive predictions(Low False Positive Rate) and demonstrates good generalization performance(Accuracy of 80% on unseen dataset).


## 2. Data Understanding

The dataset used was obtained from [Kaggle (Churn in Telecom's dataset)](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset) and comprises of **3333 rows and 21 columns**. All the features except the phone number and state have numerical values, with the rest being categorical or binary (international plan, voice mail plan, and churn). The churn column will be used as our target variable 

This is a binary classification problem where the goal is to predict the likelihood of a customer churning and the **churn column** will be represented by **1 - True** and **0 - False**

|Dataset Coumns|about|
|:------|------|
|State|Represents the states in the USA|
|Account length|represents the length of time (in seconds or minutes) that a customer's account has been active.|
|Area code|Geographic area code of a customer's telephone number.|
|Phone number|represents the telephone number of a customer.|
|International plan|represents whether a customer has subscribed to an international call plan or not. It can have either "Yes" or "No" values.|
|voice mail plan|represents whether a customer has subscribed to a voice mail plan or not. It can have either "Yes" or "No" values.|
|Number vmail messages|represents the number of voice mail messages left by a customer.|
|Total day minutes|represents the total amount of time (in minutes) that a customer has spent on daytime calls.|
|Total day calls|represents the total number of calls that a customer has made during the day.|
|Total day charge|represents the total charge for daytime calls made by a customer.|
|total eve minutes|represents the total amount of time (in minutes) that a customer has spent on evening calls.|
|total eve calls|represents the total number of calls that a customer has made in the evening.|
|total eve charge|represents the total charge for evening calls made by a customer.|
|total night minutes|represents the total amount of time (in minutes) that a customer has spent on night calls.|
|total night calls|represents the total number of calls that a customer has made at night.|
|total night charge|represents the total charge for night calls made by a customer.|
|total intl minutes|represents the total amount of time (in minutes) that a customer has spent on international calls.|
|total intl calls|represents the total number of international calls made by a customer.|
|total intl charge| represents the total charge for international calls made by a customer.|
|customer service calls|represents the number of customer service calls made by a customer.|
|churn|represents whether a customer has cancelled their service or not. It can have either "True" or "False" values.|

## 3. External Dataset Validation
The Telecommunication industry continues to face a major and costly challenge in the form of customer churn. A recent research study conducted in 2018 by [Analysis Mason](https://www.analysysmason.com/globalassets/x_migrated-media/media/analysys_mason_ssa_mobile_satisfaction_sample_jun2018_rdmm03.pdf), a consulting and research company, highlights this issue. The study, titled **"Connected Consumer 2017: Mobile Customer Satisfaction and Churn in Sub-Saharan Africa**," was led by senior analyst Karim Yaici and research director Stephen Sale.

According to the study, the intention to churn among telecommunication subscribers in the sub-Saharan African region ranged from **9% to 16% across all operators surveyed**. This figure is in line with churn rates in other regions, but lower compared to the neighboring Middle East and Africa (MENA) region, where the intention to churn within 6 months was recorded at an average of 22%.

The study also found that customer service had a significant impact on churn for subscribers in South Africa, where the average churn rate was 17%. This effect was much greater compared to the other countries covered, which may reflect the differences in market maturity in the region. The findings from this study serve as external validation for the importance of customer service in reducing churn in the telecommunication industry.

## 4. Modeling
The Churn classification problem is tackled with approximately 6 algorithms and tuning the best two models. some of the used models are:
 * Logistic Regression Classifier model which is our vanila/baseline model - works by finding the best line that separates the two classes in a high-dimensional space.
 * Adaboost model -  idea is to give more weight to difficult-to-classify points and improve the overall performance of the model.
 * Gradient Boosting model -known for its high accuracy and performance
 * Random Forest model - tends to reduce overfitting, which is a common issue with decision trees.
 * Decision Tree model
 * Hyperparameter tuning of the Decision Tree model
 * Hyperparameter tuning of the Random Forest model

Random forest and tunned random forest emerged as the top-performing model, boasting higher prediction accuracy and superior discrimination between outcomes. Notably, it exhibited a relatively high recall, effectively identifying most potential churners while minimizing false negatives. Additionally, it maintained a low false positive rate, minimizing erroneous flagging of customers unlikely to churn

## 5. Conclusion.

The random forest model achieved an accuracy of 0.95 and a weighted average of 0.95 in cross-validation (k=5) for predicting churn rate. Precision, recall, and f1-score for class 0 (not churned) were 0.97. For class 1 (churned), they were 0.82. The model performed well overall, with slightly better metrics for class 0 predictions. Overall, the random forest model proved to be the most effective for predicting churn rate.


## 6. Reccomendations.

Feature Engineering: Enhance prediction accuracy by introducing new features such as average daily/monthly charge or call duration. These insights can provide a deeper understanding of customer behavior and aid in churn prediction.

Data Collection: Utilize customer satisfaction surveys to gather feedback on various aspects like network coverage and customer service. Additionally, collecting personal data such as age, gender, and marital status can facilitate the creation of tailored plans that better suit individual needs and preferences.

Competitive Pricing: To ensure customer satisfaction and retention, it's imperative to offer competitive pricing and packages. By providing value for money, customers are more likely to remain loyal to the company rather than seeking alternatives.

Loyalty Programs: Implementing loyalty programs can be a valuable strategy for reducing churn. By rewarding long-term customers with incentives and rewards, the company can foster a sense of loyalty and encourage customers to continue their relationship with the brand. These programs not only incentivize retention but also enhance customer satisfaction and engagement.


### Repository Guide ###

Notebook: https://github.com/KMalinga

Dataset: https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download
