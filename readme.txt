Prediction Models for Mental Health Analysis
This project builds and evaluates machine learning models to predict depression (binary classification) based on personal, mental health, and socioeconomic features. The dataset includes preprocessed data for 2020, 2021, and 2022.

Project Overview
We implemented and compared the following models:

Baseline Model: A simple benchmark using the majority class.
Random Forest (RF): Handles complex interactions and provides feature importance.
Logistic Regression (LR): Establishes an interpretable baseline.
XGBoost: Optimizes performance through gradient boosting.
Support Vector Machine (SVM): Effective in handling non-linear relationships but computationally intensive.

File Structure: 

The dataset is available in the below link to a drive folder
https://drive.google.com/drive/folders/1GrNV6tnajLwHg7lJyXaYaFYlrDmWBQB7?usp=sharing
mhcld_puf_2020.csv: Dataset for 2020
mhcld_puf_2021.csv: Dataset for 2021
mhcld_puf_2022.csv: Dataset for 2022

Code(without SVM).ipynb:

Contains data preprocessing and implementation of Baseline, Random Forest, Logistic Regression, and XGBoost models.
These models are computationally efficient and produce results quickly.

Code(SVM).ipynb:

Includes only the Support Vector Machine (SVM) model implementation.
SVM is time-consuming to train, so it was separated into its own file for workflow efficiency.
Evaluation Metrics
The following metrics were used to evaluate model performance:

Accuracy: Measures overall correctness.
Precision: Proportion of positive predictions that are correct.
Recall: Proportion of actual positives correctly identified.
F1-Score: Balances precision and recall.
Confusion Matrix: Provides a detailed breakdown of predictions.
ROC Curve and AUC: Analyzes the trade-off between sensitivity and specificity.

Key Results
Baseline Model: Accuracy ~67%, sets a minimum benchmark.
Random Forest: Achieved 81.53% accuracy, highlighting key features like BIPOLARFLG_1, SCHIZOFLG_1, and NUMMHS.
Logistic Regression: Accuracy refined to 81.23% after removing dominant features.
XGBoost: Accuracy is about 82.61%. Balanced performance, key features include ANXIETYFLG_1 and TRAUSTREFLG_1.
SVM: Accuracy is about 80.03%.

Feature Importance
Logistic Regression: State Indicators (e.g., New Hampshire, South Carolina)
Random Forest: Bipolar Disorder, Schizophrenia Disorder, Education, Marital Status
XGBoost: Anxiety Disorder, Trauma- and Stressor-related Disorders, Education
SVM: Schizophrenia Disorder, Bipolar Disorder, Other Mental Disorder, Conduct Disorder

How to Run the Code
Install Required Libraries:
pip install pandas numpy scikit-learn xgboost matplotlib seaborn

Run Code(without SVM).ipynb:
Processes the data and trains the Baseline, Random Forest, Logistic Regression, and XGBoost models.

Run Code(SVM).ipynb:
Includes the SVM model training and evaluation. Note that SVM may take longer depending on your system.
 
Conclusion
By splitting the code into two files, we efficiently balanced computational time and workflow. The project demonstrates how different models can provide complementary insights into feature importance and prediction accuracy.
