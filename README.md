# Admission Prediction Analysis

### Statistical Summary

Here is the statistical summary of the dataset's features:

| Feature             | Count | Mean  | Std Dev | Min | 25th Percentile | Median | 75th Percentile | Max  |
|---------------------|-------|-------|---------|-----|-----------------|--------|-----------------|------|
| GRE Score           | 400   | 316.81| 11.47   | 290 | 308             | 317    | 325             | 340  |
| TOEFL Score         | 400   | 107.41| 6.07    | 92  | 103             | 107    | 112             | 120  |
| University Rating   | 400   | 3.09  | 1.14    | 1   | 2               | 3      | 4               | 5    |
| SOP                 | 400   | 3.40  | 1.01    | 1   | 2.5             | 3.5    | 4               | 5    |
| LOR                 | 400   | 3.45  | 0.90    | 1   | 3               | 3.5    | 4               | 5    |
| CGPA                | 400   | 8.60  | 0.60    | 6.8 | 8.17            | 8.61   | 9.06            | 9.92 |
| Research            | 400   | 0.55  | 0.50    | 0   | 0               | 1      | 1               | 1    |
| Chance of Admit     | 400   | 0.72  | 0.14    | 0.34| 0.64            | 0.73   | 0.83            | 0.97 |

### Key Insights

- **GRE Scores**: Reflect a strong applicant pool, with an average GRE score of 316.81.
- **TOEFL Scores**: Indicate good English proficiency among the candidates with an average score of 107.41.
- **University Rating**: Average rating is slightly above middle indicating a moderately competitive field of applicants.
- **SOP and LOR**: Suggest that candidates have good presentations and recommendations to support their applications.
- **CGPA**: The high average CGPA of 8.60 points towards excellent academic backgrounds of applicants.
- **Research Experience**: Over half of the applicants have research experience, highlighting its importance in the admission process.
- **Chance of Admit**: With an average chance of 72%, the data reflects a positive outlook for prospective students.


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

| Model                   | Accuracy | Precision | Recall | ROC-AUC Score |
|-------------------------|----------|-----------|--------|---------------|
| Linear Regression       | 93%      | 0.93      | 0.93   | 0.8825        |
| Random Forest Classifier| 73%      | 0.73      | 0.73   | 0.7290        |
| Decision Tree           | 93%      | 0.93      | 0.93   | -             |
| KNN (Best K Value: 3)   | 90%      | -         | 0.85   | 0.8874        |
| SVM                     | 91%      | 0.92      | 0.91   |               |


## Conclusion

Through the comparison of various machine learning models to predict the likelihood of student admissions, it has been determined that the **Linear Regression** and **Decision Tree** models exhibit the highest accuracy at 93%. Both models also show a strong balance between precision and recall, indicating that they are well-tuned for both positive and negative classification. 

However, the **Linear Regression** model slightly edges out with a higher ROC-AUC score of 0.8825, compared to the Decision Tree model where the ROC-AUC score was not provided. The ROC-AUC score is particularly important as it measures the trade-off between the true positive rate and false positive rate, providing insight into the model's capability to distinguish between classes.

In light of this analysis, the **Linear Regression** model is recommended for implementation due to its high accuracy and superior ROC-AUC score, suggesting it is better at handling varied thresholds and providing a more reliable measure of performance across different possible classification cut-offs.

It's worth noting that while the **KNN** model showed a competitive ROC-AUC score, it was slightly lower in accuracy, and specific precision and recall metrics were not provided for a full comparison. The **SVM** model showed promising results as well but fell short in comparison to the Linear Regression model in terms of the overall balance of metrics.

The decision on the best model also considered the simplicity and interpretability of the models, where Linear Regression provides an easy-to-understand model with coefficients that reflect the impact of each feature on the admission chances, adding to its practical appeal.

## Contributions

Contributions are encouraged following the outlined guidelines.
