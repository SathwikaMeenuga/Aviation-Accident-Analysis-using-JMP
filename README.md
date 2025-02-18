Aviation-Accident-Analysis-using-JMP

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Overview**

This project analyzes aviation accident data from the National Transportation Safety Board (NTSB) database to assess the likelihood of serious or fatal injuries in crashes involving different aircraft manufacturers. The goal is to provide insights into safety trends and highlight areas where manufacturers can improve safety measures.

**Dataset**

Rows: 87,282

Columns: 31

Source: National Transportation Safety Board (NTSB) records

Each row represents a separate accident, including:

Location and airport details

Aircraft information

Injury severity and aircraft damage

Weather conditions and accident cause

Investigation findings
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Approach**:

We primarily relied on statistical methods to analyze the dataset. Various machine learning models were also implemented to predict accident outcomes based on aircraft manufacturer and weather conditions. The target variable was the percentage of serious or fatal injuries in an accident.

**Data Preprocessing:**

Several data cleaning and transformation steps were performed:

Irrelevant Columns Removed: ID numbers, location names, and other non-influential fields.

Recoded Variables:

Weather Condition and Engine Type missing values were categorized as 'Unknown'.

Injury Severity recoded into 'Fatal' and 'Non-Fatal'.

Target Variable Creation: A binary column indicating whether an accident resulted in serious or fatal injuries.

**Data Partitioning:**

50% Training

30% Validation

20% Test


**Model Performance:**
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

We applied multiple modeling approaches, including Neural Networks, Naïve Bayes, Decision Trees, Boosted Trees, K-Nearest Neighbors (KNN), and Discriminant Analysis.
**
Neural Network**

Misclassification rate: 14.3% (Training), 15.1% (Validation), 15.1% (Test)

Accuracy: 85.7% (Training), 84.9% (Validation), 84.9% (Test)

Lift: 2.60 (Training), 2.61 (Validation), 2.61 (Test)

**Naïve Bayes
**
Misclassification rate: 14.8% (Training), 15.4% (Validation), 15.2% (Test)

Accuracy: 85.2% (Training), 84.6% (Validation), 84.9% (Test)

Lift: 2.62 (Training), 2.59 (Validation), 2.61 (Test)

ROC Curve AUC: 0.888 (Training), 0.879 (Validation), 0.881 (Test)

**K-Nearest Neighbors (KNN)
**
Optimal K-value: 10

Accuracy: 84.7% (Training), 84.8% (Validation)

Lift: 2.67 (Training), 2.68 (Validation)

**Decision Trees and Boosted Trees
**
The best decision tree model achieved ~14% misclassification rate.

Boosted Trees improved performance slightly by allowing more variables to contribute.

**Discriminant Analysis
**
Misclassification rate: 14.94% (Training), 15.17% (Validation), 15.01% (Test)

Accuracy: 85.06% (Training), 84.83% (Validation), 84.99% (Test)



******Conclusion******
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------


Weather conditions play a crucial role: Fatalities were more common in Visual Meteorological Conditions (79.23%).

Aircraft damage is highly correlated with fatalities: 69.77% of fatal crashes involved a destroyed aircraft.

Personal flights had the highest accident count: While only 32.57% of personal-use aircraft crashes were fatal, they accounted for 63.54% of overall fatalities.

Model performance was consistent across different approaches: Most models achieved an accuracy of ~85% with a misclassification rate of ~15%.

Future Work: Investigate additional factors such as pilot experience, maintenance history, and flight duration to improve model accuracy.

**Tools Used**:

JMP (Statistical Analysis & Modeling)

Data Cleaning and Transformation

Machine Learning Models (Neural Networks, Naïve Bayes, Decision Trees, etc.)
