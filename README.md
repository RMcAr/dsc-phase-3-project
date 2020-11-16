# Modelling Customer Churn for SyriaTel

## Introduction
We are tasked with constructing a model that will best predict customer churn for SyriaTel, a telecommunications company. 

## Objectives
- Construct a classification model
- Explore trends on customer data
- Provide recommendations to SyriaTel for improving customer retention

## Data
Data is split into three types:
- Customer Data
- Usage Data
- Plan Data

## Models
We fitted two types of models: Logistic Classification and Random Forest Classification.
- Logistic Regression did not perform well, falling well below any acceptable score. 
- Random Forest classification performed the best when location features were not taken into account. 

## Findings
### Optimal Model:
We found that a Random Forest model, optimized through a GridSearch, performed best when ignoring location data. Our initial fit showed that the feature importances of location data was extremely small compared to other features. 
### Customer Trends
We found that customers are satisfied with the voicemail plan, while dissatisfied with the international plan. We also found that location does not contribute to churn, and that customers who pay more on average do not have other identifying factors. 
### How to Improve Retention
#### 1. Investigate how our International Plan can be improved. 
* We found that of customers enrolled in the International Plan, 42% decided to leave SyriaTel. This suggests that customers are very displeased with our international service. 
* We also found that international service subscribers pay roughly the same amount for international calls than their non-enrolled counterparts. Giving these subscribers a greater discount on international calls may improve our international plan performance, contributing to greater customer retention. 


#### 2. Continue attempting campaigns!
* We found that a promotional campaign was underway during the time period our data was collected on. This was inferred based on the bimodal distribution of churned customers' total charges, and the slightly right skewed distribution of account length. The relationship between these two predictors suggests that the campaign was for new customers who enjoyed a discount for an introductory period. 
* While this campaign contributes to churn once this intro period is over, it is better to "take two steps forward and one step back" in this scenario. 
* Some campaigns to consider, based upon feature importance of our final model:
    - Offer at-risk customers a **trial voicemail plan**. From our EDA, customers are much less likely to churn if they are subscribed in this plan. 
    - Offer at-risk customers a **discount on their monthly charge**. While this is somewhat obvious, total charge was the single greatest feature in our final model and should not be understated. 
    - Offer **loyalty rewards** to customers with history with SyriaTel. This will help protect SyriaTel from campaigns of competing companies who may be offering our customers introductory offers (as we should be doing to their customers as well!)
#### 3. Improve our Customer Service Experience
- We found that the number of customer service calls a subsciber has to make is the second greatest feature in importance. While it is more difficult to make a customer happier with their monthly bill without taking a direct hit to profits, improving a customer's experience with our staff is not difficult to imnprove. We can accomplish this by:
    - Prioritizing the minimization of customer service calls through agent responsibility. Any customer that needs to call more than 5 times in one single cycle is not having their needs met by our service agents. These situations must be addressed sooner before our customer decides to leave on the basis of bad customer service. 
    - Providing alternatives to our customers to manage their accounts. We can add mobile, online, or automated phone accessibility quite easily, and the more self-service a customer can accomplish will decrease the burden upon our service agents as well as the need for their expert assistance. 
### Futher Investigations
Once SyriaTel is finished formulating and putting a campaign forth, we will need to complete futher investigations to measure the efficacy of these campaigns and of our constructed model. 
### Repo Structure