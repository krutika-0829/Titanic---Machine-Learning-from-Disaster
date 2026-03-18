# Titanic---Machine-Learning-from-Disaster
Using multiple classification models to predict survival of passengers and Understand which factors has great impact.

# Problem Statement
The goal of this project is to build a classification model that predicts whether a passenger survived the Titanic disaster based on features like:
Age,Sex,Passenger class (Pclass),Fare,Family information.

# Dataset Overview
The dataset contains passenger details such as:
Feature	Description
Survived	Target variable (0 = No, 1 = Yes)
Pclass	Ticket class (1st, 2nd, 3rd)
Sex	Gender
Age	Age of passenger
SibSp	Siblings/Spouses aboard
Parch	Parents/Children aboard
Fare	Ticket fare
Embarked	Port of embarkation

# Exploratory Data Analysis (EDA)

Key observations:
-Females had significantly higher survival rates.
-Higher class passengers (Pclass = 1) survived more.
-Fare is strongly related to passenger class
-Some features like Ticket and PassengerId showed no meaningful pattern

# Feature Engineering

-New features created to improve model performance:
-FamilySize = SibSp + Parch + 1
-IsAlone = Whether passenger is traveling alone
-Fare_per_person = Fare / FamilySize
These features help the model capture hidden relationships in the data.

# Models Used

The following models were trained and evaluated:

Logistic Regression
K-Nearest Neighbors
Decision Tree
Random Forest

# Model Evaluation

Evaluation metrics used:
Accuracy
Precision
Recall
Confusion Matrix

Special focus was given to recall, to ensure most survivors are correctly identified.

# Key Insight: Threshold Tuning
Instead of using the default threshold (0.5), the classification threshold was adjusted:

0.5 → default
0.4 → improved recall

This helped:
-Reduce false negatives
-Increase detection of actual survivors

# Final Model

The best performing model:

Logistic Regression (with feature scaling and threshold tuning)

Reason:
Performed consistently across metrics
Provided better recall compared to other models
Suitable for relatively small and structured dataset

Results (example)
Metric	Value
Accuracy	~0.80
Recall	Improved after threshold tuning
Precision	Slightly decreased (expected trade-off)
The focus was not just on accuracy, but on understanding model behavior and improving predictions thoughtfully.
