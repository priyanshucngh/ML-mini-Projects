# 🎓 Student Academic Performance Prediction Using Machine Learning

## 📌 Project Overview

This project focuses on predicting students' academic performance using Machine Learning classification techniques.

The system analyzes student-related attributes such as study time, absences, previous academic failures, age, parental education, and other academic and social factors to classify students into three performance categories: **At Risk, Average, and Good**.

The primary objective is to identify students who may be at risk of poor academic performance and help educators understand the factors associated with students' academic outcomes.

This project was developed individually as part of a Machine Learning mini-project.

## 🎯 Objectives

- Analyze student academic performance using Machine Learning.
- Perform data preprocessing and Exploratory Data Analysis (EDA).
- Identify relationships between student attributes and final academic grades.
- Classify students into different academic performance categories.
- Implement and evaluate Decision Tree and Random Forest classifiers.
- Compare model performance using classification metrics.
- Identify important features influencing academic performance.

## 📊 Dataset Description

The project uses the `student-por.csv` dataset.

**Dataset Details:**
- Total Records: 649
- Total Original Features: 33
- Dataset Type: Structured Data
- Prediction Type: Multi-class Classification

The dataset contains various student-related attributes, including academic, demographic, family, and social information.

## 🏷️ Performance Categories

The target variable `Performance` is created using the final grade (`G3`).

Students are classified into three categories based on the following conditions:

| Final Grade (G3) | Performance Category |
|---|---|
| G3 ≤ 9 | At Risk |
| 10 ≤ G3 ≤ 13 | Average |
| G3 > 13 | Good |

**Category Distribution:**

| Category | Number of Students |
|---|---:|
| At Risk | 100 |
| Average | 355 |
| Good | 194 |
| **Total** | **649** |

## 🛠️ Technologies & Libraries Used

- **Python** – Programming language
- **Jupyter Notebook** – Development environment
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical computations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical data visualization
- **Scikit-learn** – Machine Learning model development and evaluation

## 🔍 Project Workflow

### 1. Data Loading and Inspection
- Imported the dataset using Pandas.
- Displayed the first five records.
- Checked dataset dimensions and column names.
- Examined dataset information and statistical summaries.

### 2. Data Preprocessing
- Checked for missing values.
- Checked duplicate records.
- Created performance categories using final grades.
- Removed `G1`, `G2`, `G3`, and `Performance` from the input features.
- Separated input features and target variable.
- Applied One-Hot Encoding to categorical variables.

### 3. Exploratory Data Analysis (EDA)

The following visualizations were performed:

- Student Academic Performance Distribution
- Study Time vs Final Grades
- Impact of Student Absences on Final Grades
- Previous Academic Failures vs Performance
- Correlation Heatmap of Student Attributes

### 4. Feature Selection
- Selected 30 original input features.
- Excluded grade columns (`G1`, `G2`, `G3`) from model inputs.
- Converted categorical variables into numerical representations using One-Hot Encoding.
- Obtained 39 encoded input features.

### 5. Train-Test Split

The dataset was divided into training and testing sets using an 80:20 ratio.

- Training Records: 519
- Testing Records: 130
- Random State: 42
- Stratification: Applied

## 🤖 Machine Learning Algorithms

Two classification algorithms were implemented:

### 1. Decision Tree Classifier
A tree-based classification algorithm used to predict student academic performance categories based on the selected input features.

### 2. Random Forest Classifier
An ensemble learning algorithm that combines multiple decision trees to perform classification.

**Model Configuration:**
- Number of Estimators: 100
- Random State: 42

## 📈 Model Evaluation

Both models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Classification Report

### Model Performance Comparison

| Evaluation Metric | Decision Tree | Random Forest |
|---|---:|---:|
| Accuracy | 46.15% | 63.08% |
| Macro Precision | 39.81% | 61.33% |
| Macro Recall | 37.54% | 47.87% |
| Weighted Precision | 44.87% | 62.18% |
| Weighted Recall | 46.15% | 63.08% |

### Classification Performance

**Decision Tree Accuracy:** 46.15%

**Random Forest Accuracy:** 63.08%

The Random Forest Classifier achieved better overall accuracy than the Decision Tree Classifier on the test dataset.

### Confusion Matrix Analysis

Confusion matrices were generated for both classifiers to examine their classification performance across the three student performance categories.

### Feature Importance Analysis

The Random Forest model was used to identify the top 10 important features influencing student academic performance.

The top features identified were:

1. Absences
2. Age
3. Medu (Mother's Education)
4. Health
5. Goout
6. Failures
7. Walc
8. Freetime
9. Fedu (Father's Education)
10. Famrel

## 📌 Conclusion

The project demonstrates the application of Machine Learning classification techniques for student academic performance prediction.

Two classification models, Decision Tree and Random Forest, were implemented and evaluated.

The Random Forest Classifier achieved an accuracy of **63.08%**, outperforming the Decision Tree Classifier, which achieved **46.15%** accuracy.

Feature importance analysis highlighted student absences, age, parental education, health, and other student-related attributes as important predictors in the trained Random Forest model.

One limitation observed was the relatively low recall of the At Risk category (15%) in both models. This indicates that identifying students at risk remains a challenging aspect of the current implementation.


## 👨‍💻 Author

**Priyanshu Kumar Singh**

---

**Project Type:** Individual Machine Learning Mini-Project

**Domain:** Machine Learning | Data Analysis | Educational Data Mining

⭐ If you find this project interesting, feel free to explore the repository!
