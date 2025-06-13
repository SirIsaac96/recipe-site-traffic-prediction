# Recipe Site Traffic Prediction with Machine Learning

## Project Overview

This repository contains the code and documentation for my DataCamp Certification Practical Exam project, Recipe Site Traffic Prediction. The objective is to predict which recipes will drive high traffic to a website’s homepage, targeting an accuracy of 80%. By identifying high-traffic recipes, the model aims to increase website traffic and subscriptions. The dataset used for training, validation, and testing was provided by DataCamp.

### Workflow

1. **Data Validation and Cleaning**:
    - Inspected dataset structure and addressed inconsistencies (e.g., corrected 'Chicken Breast' to 'Chicken' in the category column).
    - Handled missing values in numerical columns (calories, carbohydrate, sugar, protein) and converted 'servings' to numeric.
    - Replaced missing 'high_traffic' values with 'Low' to indicate low traffic.
2. **Exploratory Data Analysis (EDA)**:
    - Analyzed distributions of numerical features and relationships with the target variable ('high_traffic').
    - Visualized category-wise traffic trends to identify high-traffic recipe categories.
3. **Data Preprocessing**:
    - Encoded categorical variables ('category', 'servings') using one-hot encoding.
    - Standardized numerical features for model compatibility.
4. **Model Development**:
    - Built a baseline Logistic Regression model to predict high-traffic recipes.
    - Developed a Random Forest Classifier as a comparison model to evaluate performance improvements.
    - **Key Finding**: The logistic regression model outperforms the random forest classifier. It provides a better recall (89%) and a higher F1-score (83%), ensuring that most high-traffic recipes are correctly predicted while maintaining a lower rate of false positives.
5. **Evaluation**:
    - Evaluated both models using accuracy, precision, recall, and F1-score.
    - Compared model performance with confusion matrices and classification reports to assess trade-offs.
    - The Random Forest Classifier was tested to explore potential improvements in predictive power, but the Logistic Regression model showed superior performance.

## Recommendations
    - Proposed deploying the Logistic Regression model for its superior recall (89%) and F1-score (83%) to automate recipe selection.
    - Suggested a dashboard for monitoring Popular Recipe Success Rate (PRSR) on a daily, weekly, and monthly basis.
    - Recommended automated alerts for PRSR drops below 75% and continuous model improvement through additional data collection, feature engineering, and hyperparameter tuning for both models.

## Key Results
    - The Logistic Regression model effectively identifies ~89% of high-traffic recipes with an F1-score of 83%, supporting a potential 40% increase in website traffic.
    - The Random Forest Classifier was evaluated but underperformed compared to Logistic Regression, as detailed in the notebook.
    - The model minimizes the appearance of unpopular recipes, enhancing user engagement and subscriptions.
    - Visualized results with confusion matrices and classification reports.

## Dependencies

    - Python
    - pandas
    - numpy
    - scikit-learn
    - matplotlib
    - seaborn
    - jupyter

## License
- This project is intended for academic and educational use.

## Acknowledgments

DataCamp for providing the dataset and project framework.
