# ✈ Aviation Accident Analysis using JMP

 Overview
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
This project analyzes aviation accident data from the National Transportation Safety Board (NTSB) database to assess the likelihood of serious or fatal injuries in crashes involving different aircraft manufacturers.

🔹 The goal is to provide insights into safety trends and highlight areas where manufacturers can improve safety measures.

📂 Dataset

📊 Rows: 87,282

📊 Columns: 31

📊 Source: National Transportation Safety Board (NTSB) records

Each row represents a separate accident, including:

✔ Location and airport details

✔ Aircraft information

✔ Injury severity and aircraft damage

✔ Weather conditions and accident cause

✔ Investigation findings

🛠 Approach
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
We primarily relied on statistical methods to analyze the dataset. Various machine learning models were also implemented to predict accident outcomes based on aircraft manufacturer and weather conditions.

🔹 The target variable was the percentage of serious or fatal injuries in an accident.

🧹 Data Preprocessing
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
✅ Irrelevant Columns Removed

ID numbers, location names, and other non-influential fields were dropped.

✅ Recoded Variables

Weather Condition and Engine Type missing values were categorized as 'Unknown'.

Injury Severity was recoded into 'Fatal' and 'Non-Fatal'.

A binary target variable was created to indicate whether an accident resulted in serious or fatal injuries.

✅ Data Partitioning

🔹 50% Training
🔹 30% Validation
🔹 20% Test

📈 Model Performance
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
We applied multiple modeling approaches, including:
✔ Neural Networks
✔ Naïve Bayes
✔ Decision Trees & Boosted Trees
✔ K-Nearest Neighbors (KNN)
✔ Discriminant Analysis

🤖 Neural Network

Neural Networks are used for capturing complex patterns and nonlinear relationships in the data. They are particularly useful in accident prediction, where multiple factors influence the severity of an accident.

🔹 Misclassification Rate:

Training: 14.3%

Validation: 15.1%

Test: 15.1%

🔹 Accuracy:

Training: 85.7%

Validation: 84.9%

Test: 84.9%

🔹 Lift:

Training: 2.60

Validation: 2.61

Test: 2.61

📊 Naïve Bayes

Naïve Bayes is effective in predicting accident severity by estimating probabilities based on conditional independence assumptions. It is particularly useful when working with categorical features such as weather conditions and aircraft type.

🔹 Misclassification Rate:

Training: 14.8%

Validation: 15.4%

Test: 15.2%

🔹 Accuracy:

Training: 85.2%

Validation: 84.6%

Test: 84.9%

🔹 Lift:

Training: 2.62

Validation: 2.59

Test: 2.61

🔹 ROC Curve AUC:

Training: 0.888

Validation: 0.879

Test: 0.881

A high AUC score (close to 1) indicates that the model effectively differentiates between fatal and non-fatal accidents, making it a reliable classification tool.

📌 K-Nearest Neighbors (KNN)

KNN predicts accident severity by comparing new accident data with similar past accidents. It is particularly useful in cases where similar patterns exist in historical crashes.

✔ Optimal K-value: 10

✔ Accuracy:

Training: 84.7%

Validation: 84.8%

✔ Lift:

Training: 2.67

Validation: 2.68

The K-value (10) ensures a balance between bias and variance, preventing overfitting while maintaining accurate predictions.

🌳 Decision Trees and Boosted Trees

Decision Trees help identify key factors leading to fatal accidents, while Boosted Trees enhance prediction accuracy by combining multiple weak models.

✔ Best Decision Tree Model: Achieved ~14% misclassification rate.

✔ Boosted Trees: Improved performance slightly by allowing more variables to contribute.

Decision Trees are particularly valuable in this analysis as they offer interpretable rules, making it easier to understand why certain accidents result in fatalities.

📉 Discriminant Analysis

Discriminant Analysis is used to separate fatal and non-fatal crashes by identifying optimal decision boundaries based on feature distributions.

🔹 Misclassification Rate:

Training: 14.94%

Validation: 15.17%

Test: 15.01%

🔹 Accuracy:

Training: 85.06%

Validation: 84.83%

Test: 84.99%

This model helps in understanding the key differentiators between high-risk and low-risk crashes while maintaining a simple, interpretable structure.

🛬 Conclusion
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
📍 Weather conditions play a crucial role

Fatalities were more common in Visual Meteorological Conditions (79.23%).

📍 Aircraft damage is highly correlated with fatalities

69.77% of fatal crashes involved a destroyed aircraft.

📍 Personal flights had the highest accident count

Personal-use aircraft crashes accounted for 32.57% of fatal accidents but 63.54% of overall fatalities.

📍 Model performance was consistent across different approaches

Most models achieved ~85% accuracy with a ~15% misclassification rate.

🔮 Future Work
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Investigate additional factors such as pilot experience, maintenance history, and flight duration to improve model accuracy.

🛠 Tools Used
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
✔ JMP (Statistical Analysis & Modeling)

✔ Data Cleaning & Transformation

✔ Machine Learning Models (Neural Networks, Naïve Bayes, Decision Trees, etc.)
