# TikTok-Project-Lab

# PROJECT TITLE: Predicting User Verified Status Based on Video Features

# Project Overview
This project focuses on building a logistic regression model to predict whether a TikTok user is verified based on video characteristics. By understanding the relationship between video features and user verification status, TikTok aims to improve its ability to prioritize user reports and manage content more effectively. The project demonstrates expertise in exploratory data analysis (EDA) and regression modeling.

# Motivation
Predicting user verification status helps TikTok manage user-generated content more efficiently. By identifying which videos are more likely to come from verified users, TikTok can prioritize reports and handle content issues more effectively. This model can also inform the final model for classifying videos as claims or opinions.

# Dataset
Source: Collected from TikTok’s API or data sources.

Number of Records: (19382, 12)

# Features: 
## The dataset includes the following variables:

Video Duration

Video View Count

Video Share Count

Video Download Count

Video Comment Count

Claim Status (Target Variable)

Author Ban Status

User Verified Status (Outcome Variable)

# Data Preprocessing

Renaming and standardizing columns

Handling missing values

Removing duplicates

Addressing outliers

Encoding categorical variables (e.g., claim_status and author_ban_status)

# Exploratory Data Analysis (EDA) Insights

Correlations:

Strong correlation observed between video_view_count and video_like_count (0.86). To avoid multicollinearity, video_like_count was excluded from the model.
Video Metrics: Key video metrics like video_view_count, video_share_count, video_download_count, and video_comment_count were used as features.

Verified Status:

Users who are verified tend to post longer videos, and this feature showed a positive association with verification status.
Models and Results
# 1. Logistic Regression Model

The logistic regression model was built to predict whether a user is verified based on video characteristics.

Performance Metrics:

Precision: 61%

Recall: 84%

Accuracy: 65%

# Key Insights:

Model Performance: 

The model achieved acceptable recall (84%) but had moderate precision (61%) and accuracy (65%). This suggests that while the model is good at identifying verified users, it may misclassify some non-verified users.
Feature Impact: 

Each additional second of video is associated with a 0.009 increase in the log-odds of the user being verified. Other features have smaller estimated coefficients, indicating their smaller impact on verification status.

# Conclusion and Recommendations
The logistic regression model provides useful insights into the factors associated with user verification status. Key takeaways include:

Longer Videos: 

Longer videos are positively associated with the likelihood of a user being verified.

Feature Selection:

Excluding highly correlated features (e.g., video_like_count) helps address multicollinearity issues.

Model Performance:

The model shows decent performance but could be improved for better precision.

Recommendations:

Feature Refinement:

Continue refining feature selection to improve model accuracy and precision.

Model Enhancement:

Explore additional features or alternative models to enhance predictive power.

Monitoring:

Regularly monitor and update the model to adapt to changes in user behavior and content trends.

By implementing these strategies, TikTok can better manage and prioritize user content, leading to improved platform efficiency and user experience.

