# Admission Prediction Analysis

## Dataset Description

The dataset "Admission_Predict.csv" comprises various parameters deemed crucial during the application process for Masters Programs. The following table presents a data dictionary describing each feature:

| Feature               | Description                                           | Type       |
|-----------------------|-------------------------------------------------------|------------|
| GRE Scores            | Scores out of 340                                     | Integer    |
| TOEFL Scores          | Scores out of 120                                     | Integer    |
| University Rating     | Rating out of 5                                       | Integer    |
| SOP                   | Statement of Purpose Strength out of 5                | Float      |
| LOR                   | Letter of Recommendation Strength out of 5            | Float      |
| CGPA                  | Undergraduate GPA out of 10                           | Float      |
| Research              | Research Experience (0 for No, 1 for Yes)             | Binary     |
| Chance of Admit       | Likelihood of admission (ranging from 0 to 1)         | Float      |

Access the dataset on Kaggle: [Admission Prediction Dataset](https://www.kaggle.com/datasets/adityadeshpande23/admissionpredictioncsv).

## Objective

The aim is to classify applicants based on their likelihood of admission (> 0.8 or < 0.8) and determine the most effective model for implementation, including the SVM model.

## Repository Structure

- `/notebooks` - Contains Jupyter notebooks for exploratory data analysis and machine learning modeling.
- `/data` - Contains the `Admission_Predict.csv` dataset file.

## Project Steps

### Introduction/Context

Understanding the dataset precedes exploratory data analysis, which leads to data preparation for modeling.

### Exploratory Data Analysis

I analyze the feature distributions and their relationships to the chances of admission.

### Modeling

I utilize the following machine learning models for classification:

- RandomForestClassifier
- Decision Tree
- LogisticRegression
- KNN (K-Nearest Neighbors)
- SVM (Support Vector Machine)

## Report on Models

The following table summarizes the performance of each model based on precision, recall, f1-score, and ROC-AUC score:

| Model                   | Accuracy | Precision | Recall | F1-Score | ROC-AUC Score |
|-------------------------|----------|-----------|--------|----------|---------------|
| Linear Regression       | 93%      | -         | -      | -        | 0.8825        |
| Random Forest Classifier| 73%      | -         | -      | -        | 0.7290        |
| Decision Tree           | 93%      | -         | -      | -        | -             |
| KNN (Best K Value: 3)   | 90%      | -         | -      | -        | 0.8874        |
| SVM                     | 91%      | -         | -      | -        | -             |

## Conclusion

The comparison provides insights into each model's predictive power regarding student admissions.

## Contributions

Contributions are encouraged following the outlined guidelines.
