### The goal of this project is to develop a spam detection classification model that can accurately distinguish between spam and non-spam messages. The model will be evaluated using two metrics: accuracy and a custom-defined misclassification cost.

### Data Import and Exploration:
Data is loaded from a file (presumably a CSV file) using pandas.
The dataset contains various features related to email characteristics, including word frequencies, character frequencies, and capital run lengths.
Descriptive statistics are calculated using df.describe() to get an overview of the dataset.
The target variable 'spam_or_not' has two classes: 0 (non-spam) and 1 (spam).
No missing values are present in the dataset (df.isna().sum()).

### Data Preparation:
The dataset is split into input variables (X) and the target variable (y).
The data is further divided into training and testing sets using train_test_split.
Standard scaling is applied to normalize the data.

### Model Building:
Several machine learning models are considered:

Decision Tree
Logistic Regression
K-Nearest Neighbors (KNN)
Support Vector Machine (SVM) Classifier
Random Forest Classifier
XGBoost Classifier
Simple Neural Network (NN)

### Model Evaluation - Accuracy:
Models are evaluated using nested cross-validation with the primary metric being accuracy.
Hyperparameter tuning is performed for each model using grid search.

### Model Evaluation - Misclassification Cost:
A custom misclassification cost function is defined.
Models are evaluated using nested cross-validation with the misclassification cost as the primary metric.
Best Model Selection:
The best model based on accuracy and misclassification cost is determined for each metric.
Hyperparameter tuning is performed for the selected best model.

### Evaluation Metrics:
Evaluation metrics such as precision, recall, accuracy, F1-score, ROC curve, AUC, precision-recall curve, and cumulative gain curve are calculated and visualized.

### Summary of Results:
Ensemble models (Random Forest and Light GBM Classifier) perform well in terms of accuracy and misclassification cost.
Hyperparameter tuning is performed to find the optimal parameters for the best model.
Conclusion:
The Random Forest Classifier is selected as the final model based on misclassification cost.
The model is trained with the best parameters and evaluated on the test set.
