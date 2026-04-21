# Personality Type Classification Project

This project aims to compare the performance of different machine learning models in predicting personality types. Using the open-source `personality_dataset`, an Introvert/Extrovert classification task was performed. The process included data preprocessing, model training, model evaluation, cross-validation, and hyperparameter optimization.

## Dataset Information
The project utilizes the Extrovert vs Introvert Behavior Data dataset.
* **Observation Count:** 2900
* **Features:** 7 features + 1 target variable
* **Class Distribution:** Extrovert (1491), Introvert (1409

## Models and Libraries Used
The following models were utilized for this classification task:

| Model Name | Advantage in This Study | Library |
| :--- | :--- | :--- |
| **Logistic Regression** | Strong in linear separation, fast, and interpretable. | scikit-learn |
| **KNN** | Simple, non-parametric method; captures local neighborhood relations well. | scikit-learn |
| **Decision Tree** | Presents feature effects in an explainable way via decision rules. | scikit-learn |

## Performance Metrics
The performance metrics obtained from the models are as follows:

| Model Name | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Logistic Regression** | 0.9103 | 0.8938 | 0.9255 | 0.9094 | 0.9171 |
| **KNN** | 0.9155 | 0.8923 | 0.9397 | 0.9154 | 0.9416 |
| **Decision Tree** | 0.9138 | 0.8919 | 0.9362 | 0.9135 | 0.9505 |

## Evaluation

### Cross Validation
* A 5-Fold Cross Validation was applied to the Logistic Regression model.
* F1 scores: 0.9663, 0.9315, 0.9190, 0.9132, and 0.9036, resulting in an average F1 score of 0.9267.
* The proximity of the fold results indicates that the model's generalizable performance is consistent.

### Hyperparameter Optimization
* `GridSearchCV` was applied to the KNN model.
* Best parameters: $n\_neighbors=11$, $weights=uniform$, $metric=minkowski$; best CV F1 score is 0.9375.
* Post-optimization test performance: Accuracy = 0.9155, Precision = 0.8923, Recall = 0.9397, F1 = 0.9154.
* These results demonstrate that the KNN model provides a balanced and strong performance with appropriate hyperparameters.

### General Assessment
* All three models produced high accuracy and F1 scores, and overall performances were close to each other.
* The KNN model provided the best result based on the F1 score, while the Decision Tree reached the highest value in terms of ROC-AUC.
* No significant overfitting was observed as the gap between training and test performance was not large.
* For better results, feature engineering, wider hyperparameter searching, and different models (SVM, Random Forest, XGBoost) can be attempted in future studies.
