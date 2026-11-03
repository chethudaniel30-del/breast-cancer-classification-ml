# Breast Cancer Classification Using Machine Learning

## Week 4 Project Report
**Virtual Data Science with Python Internship**

## 1. Project Overview
This project implements a supervised machine learning workflow to classify breast cancer observations as **malignant or benign** using the Wisconsin Breast Cancer Diagnostic dataset available through Scikit-learn.

Two classification algorithms, Logistic Regression and Random Forest, are trained and evaluated to compare their predictive performance.

This project is for educational purposes only and is not intended for medical diagnosis.

## 2. Technologies Used
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook
- python-docx

## 3. Dataset
The dataset contains:
- **569 observations**
- **30 numerical predictor features**
- **2 target classes**
- 357 benign observations
- 212 malignant observations

The dataset was loaded using `load_breast_cancer()` from `sklearn.datasets`. The target labels are 1 for benign and 0 for malignant.

## 4. Methodology
1. Loaded and explored the dataset.
2. Checked for missing values and duplicate records.
3. Split the data into training and testing sets using an 80:20 ratio and stratified sampling.
4. Standardised features for Logistic Regression.
5. Trained Logistic Regression and Random Forest classifiers.
6. Evaluated both models using accuracy, precision, recall, and F1-score.
7. Applied five-fold stratified cross-validation.
8. Visualised model performance and Random Forest feature importance.

## 5. Model Performance

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Test Accuracy | 98.25% | 95.61% |
| Malignant Precision | 97.62% | 95.12% |
| Malignant Recall | 97.62% | 92.86% |
| Malignant F1-score | 97.62% | 93.98% |
| Mean CV Accuracy | 97.80% | 96.26% |
| Mean CV Malignant Recall | 96.47% | 95.29% |

Logistic Regression achieved better overall results in this experiment. These results are specific to the selected dataset, model settings, and evaluation procedure.

## 6. Feature Importance
The three highest-ranked features in the Random Forest model were:
1. Worst perimeter
2. Worst area
3. Worst concave points

These features had the highest importance scores among the 30 predictors. Feature importance reflects predictive contribution and does not establish causation or clinical significance.

## 7. Repository Contents
- `Breast_Cancer_Classification.ipynb` : Jupyter Notebook containing data exploration, preprocessing, model training, evaluation, and visualisations.
- `Breast_Cancer_Classification_Report.docx` : Detailed project report.
- `visualization_1_class_distribution.png` : Target class distribution.
- `visualization_2_mean_radius.png` : Mean radius analysis.
- `visualization_3_area_smoothness.png` : Area and smoothness analysis.
- `visualization_4_logistic_confusion_matrix.png` : Logistic Regression confusion matrix.
- `visualization_5_model_comparison.png` : Comparison of evaluation metrics.
- `visualization_6_cross_validation.png` : Cross-validation results.
- `visualization_7_feature_importance.png` : Top 10 Random Forest features.

## 8. Conclusion
The project demonstrates a complete supervised machine learning workflow, including exploratory data analysis, preprocessing, model implementation, validation, evaluation, and feature-importance analysis.

Logistic Regression achieved 98.25% test accuracy and 97.80% mean cross-validation accuracy, making it the preferred model in this experiment.

## 9. Limitations and Future Work
The project uses one dataset and two classification algorithms. Future work could include hyperparameter tuning, additional classifiers, ROC-AUC analysis, precision-recall curves, and validation on independent datasets.

**Disclaimer:** This project is an educational demonstration, not a clinically validated diagnostic tool.
