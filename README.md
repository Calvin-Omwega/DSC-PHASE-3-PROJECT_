# DSC-PHASE-3-PROJECT_
Phase 3 Project
# Churn in Telecom

## Project Overview

The objective of this project is to build a binary classification model to predict whether a customer will "soon" stop doing business with SyriaTel. The goal is to leverage customer data to identify patterns and trends that signal potential churn, thereby enabling the company to implement targeted retention strategies.

# Business Understanding

Challenges:

- High Customer Churn: Telecommunications companies like SyriaTel face significant revenue loss due to customers discontinuing their services.

- Identifying At-Risk Customers: Without a reliable predictive model, it's challenging to identify customers who are likely to churn.

- Data Utilization: Effective use of customer data to predict churn requires sophisticated analysis and modeling techniques.

- Resource Allocation: Efficiently allocating resources towards retention efforts for customers most likely to churn.


# Business Objectives

The main objective of this project is to build a robust classifier to predict whether a customer will "soon" stop doing business with SyriaTel. This involves:

- Predicting Customer Churn: Develop a predictive model to identify customers at high risk of churning.

- Improving Retention Strategies: Provide actionable insights to the retention and marketing teams to tailor their strategies effectively.

- Optimizing Resources: Help the company allocate its resources more efficiently towards retaining customers most likely to churn.

- Enhancing Customer Satisfaction: By predicting churn and taking proactive measures, improve overall customer satisfaction and loyalty.

# Questions to Answer

To achieve these objectives, the following questions need to be addressed:

- What are the key factors influencing customer churn at SyriaTel?

- Can we identify patterns and trends in the data that predict customer churn?

- Which features (customer attributes, behaviors, etc.) are the most significant predictors of churn?

- How accurately can our model predict whether a customer will churn in the near future?

- What strategies can be recommended based on the model's predictions to reduce churn?

## Dataset used

Telecom's dataset csv

# Modeling

1. Logistic Regression
- Results:
    - Training Accuracy: 86.9%
    - Test Accuracy: 86.4%
    - Precision (Non-Churn): 0.88
    - Recall (Non-Churn): 0.97
    - F1-Score (Non-Churn): 0.92
    - Precision (Churn): 0.57
    - Recall (Churn): 0.26
    - F1-Score (Churn): 0.35
    - Confusion Matrix: [[551, 19], [72, 25]]

Evaluation:
- Logistic Regression shows moderate overall accuracy.
- It performs well in predicting non-churn customers but struggles significantly with predicting churn customers, as indicated by low recall and F1-score for the churn class.
- Implications for the Organization: While the model can help identify a broad segment of non-churn customers, it is not reliable enough for targeting churn prevention strategies due to its poor performance in predicting churn accurately.

2. Decision Tree
- Results:
    - Training Accuracy: 97.0%
    - Test Accuracy: 93.4%
    - Precision (Non-Churn): 0.95
    - Recall (Non-Churn): 0.98
    - F1-Score (Non-Churn): 0.96
    - Precision (Churn): 0.84
    - Recall (Churn): 0.67
    - F1-Score (Churn): 0.75
    - Confusion Matrix: [[558, 12], [32, 65]]

Evaluation:
- The Decision Tree model provides high interpretability with clear decision rules and good performance in predicting both churn and non-churn customers.
It maintains a good balance between precision and recall for the churn class.

- Implications for the Organization: The Decision Tree model is useful for understanding and explaining the factors leading to churn. Its interpretability makes it ideal for communicating with stakeholders and developing targeted strategies.

3. Random Forest
- Results:
    - Training Accuracy: 94.6%
    - Test Accuracy: 90.6%
    - Precision (Non-Churn): 0.91
    - Recall (Non-Churn): 0.99
    - F1-Score (Non-Churn): 0.95
    - Precision (Churn): 0.90
    - Recall (Churn): 0.39
    - F1-Score (Churn): 0.55
    - Confusion Matrix: [[566, 4], [59, 38]]

Evaluation:
- Random Forest shows robust performance with high overall accuracy and excellent precision.
- However, it has lower recall for the churn class compared to the Decision Tree, indicating it might miss some churn cases.
- Implications for the Organization: Random Forest can be used for more reliable predictions but is less interpretable. It’s useful for scenarios where accuracy is critical, but its predictions should be complemented with insights from more interpretable models like the Decision Tree.


## Conclusion 
Based on the analysis, modeling, and interpretation of the data, we can draw the following conclusions and recommendations for SyriaTel to address customer churn:

- Key Predictors of Churn:
Total Day Minutes and Total Day Charge: High day minutes and corresponding charges are the most significant indicators of churn. Customers with high daytime usage are more likely to consider leaving the service, possibly due to high costs.


- Model Performance
    - Decision Tree Model: Provides high interpretability with clear decision rules, making it easier to understand and act upon. The model achieves good performance with a test accuracy of 93.4%, making it a reliable tool for predicting churn.

    - Random Forest Model: Offers slightly better overall predictive performance due to its robustness and ability to reduce overfitting. However, it is less interpretable than the Decision Tree.