# 🧠 Obesity Level Prediction Using Machine Learning

## 📌 Project Overview

This project develops an **end-to-end machine learning pipeline** for predicting an individual's obesity level based on demographic, dietary, physical activity, and lifestyle factors.

The problem is formulated as a **multiclass classification task**, where the target variable `NObeyesdad` represents seven different weight-status categories, ranging from **Insufficient Weight** to **Obesity Type III**.

The project demonstrates the complete machine learning workflow, including **exploratory data analysis, data preprocessing, feature engineering, model development, hyperparameter tuning, model evaluation, and model selection**.

---

## 🎯 Business Problem

Obesity is an important public health concern and is associated with various chronic health conditions and increased healthcare costs.

The objective of this project is to determine whether machine learning can be used to estimate an individual's obesity level based on measurable demographic, dietary, physical, and lifestyle characteristics.

The model uses information such as:

* Age
* Gender
* Height
* Weight
* Family history of overweight
* Eating habits
* Physical activity
* Water consumption
* Transportation habits
* Lifestyle-related factors

The goal is to develop a reliable classification model that can identify obesity levels and potentially support **early risk assessment and data-driven health analysis**.

> **Note:** This project is intended for educational and analytical purposes and should not be considered a medical diagnostic system.

---

## 📊 Dataset

The dataset used in this project is the **Estimation of Obesity Levels Based on Eating Habits and Physical Condition** dataset from the **UCI Machine Learning Repository**.

**Dataset Source:**
https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition

### Dataset Characteristics

| Attribute       | Description                   |
| --------------- | ----------------------------- |
| Records         | 2,111                         |
| Variables       | 16 input variables            |
| Target Variable | `NObeyesdad`                  |
| Problem Type    | Multiclass Classification     |
| Data Domain     | Health, Lifestyle & Nutrition |

The dataset contains demographic, dietary, physical condition, and lifestyle-related variables.

---

## 🎯 Target Variable

The target variable is:

```text
NObeyesdad
```

It contains seven obesity-related classes:

1. Insufficient Weight
2. Normal Weight
3. Overweight Level I
4. Overweight Level II
5. Obesity Type I
6. Obesity Type II
7. Obesity Type III

The objective of the machine learning models is to correctly classify individuals into one of these seven categories.

---

## 🔍 Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to understand the dataset and identify relationships between the features and obesity levels.

The analysis included:

* Dataset structure and summary statistics
* Missing-value analysis
* Duplicate-value analysis
* Distribution analysis
* Categorical feature analysis
* Numerical feature analysis
* Correlation analysis
* Target variable distribution
* Relationship between lifestyle factors and obesity levels
* Identification of important predictive variables

EDA helped identify patterns in variables such as **weight, height, physical activity, eating behavior, and family history of overweight**.

---

## ⚙️ Data Preprocessing

Several preprocessing steps were implemented before model training.

### Data Cleaning

* Checked for missing values
* Examined duplicate observations
* Reviewed data types and feature distributions
* Identified categorical and numerical variables

### Feature Transformation

Categorical variables were transformed into numerical representations using appropriate encoding techniques.

Numerical variables were scaled where required to ensure that features with different ranges could be effectively used by the machine learning algorithms.

### Imputation

Missing values were handled as part of the preprocessing pipeline to ensure that the models could work with clean and consistent input data.

---

## 🤖 Machine Learning Models

Two classification models were developed and optimized:

### 1. Logistic Regression

Logistic Regression was used as an interpretable baseline classification model.

It provides a useful balance between:

* Predictive performance
* Interpretability
* Computational efficiency

### 2. Random Forest

Random Forest was implemented as a tree-based ensemble model capable of capturing nonlinear relationships between lifestyle and demographic variables.

The model is particularly useful for identifying complex interactions between features.

---

## 🔧 Hyperparameter Optimization

Model hyperparameters were optimized using:

```text
GridSearchCV
```

Cross-validation was used during the optimization process to identify suitable hyperparameter combinations while reducing the risk of relying on a single train-validation split.

The final models were then evaluated on a separate test dataset.

---

## 📈 Model Performance

The optimized models achieved approximately **94% accuracy on the test dataset**.

### Cross-Validation Performance

**Logistic Regression**

* Cross-validation accuracy: **93.71%**

Based on the combination of predictive performance and interpretability, **Logistic Regression was selected as the preferred model**.

Both developed models demonstrated strong performance in classifying the seven obesity levels.

> Model performance should be interpreted in the context of the dataset and should not be generalized directly to real-world clinical populations without additional validation.

---

## ⭐ Key Features

The analysis identified several variables that were particularly important in predicting obesity levels.

### Important Predictive Factors

* **Weight**
* **Height**
* **Eating habits**
* **Physical activity**
* **Family history of overweight**

These variables showed strong relationships with the target obesity categories.

Weight was particularly influential because obesity classifications are closely associated with body composition and related measurements.

---

## 🔄 End-to-End Machine Learning Pipeline

The project follows a complete machine learning workflow:

```text
Raw Dataset
     ↓
Data Loading
     ↓
Data Exploration
     ↓
Data Cleaning
     ↓
EDA & Visualization
     ↓
Feature Engineering
     ↓
Encoding
     ↓
Imputation
     ↓
Feature Scaling
     ↓
Train/Test Split
     ↓
Model Development
     ↓
GridSearchCV
     ↓
Cross-Validation
     ↓
Model Evaluation
     ↓
Model Selection
     ↓
Final Predictions
```

---

## 🛠️ Tools & Technologies

The project was developed using Python and common machine learning and data analysis libraries.

### Programming Language

* Python

### Data Analysis

* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn

### Machine Learning

* Scikit-learn
* Logistic Regression
* Random Forest
* GridSearchCV
* Cross-Validation
* Feature Scaling
* Encoding
* Imputation

### Development Environment

* Jupyter Notebook

---

## 📁 Project Structure

```text
Obesity-Level-Prediction/
│
├── data/
│   └── obesity_data.csv
│
├── notebooks/
│   └── Obesity_Level_Prediction.ipynb
│
├── visualizations/
│   └── charts_and_figures/
│
├── README.md
│
└── requirements.txt
```

> The actual project structure may vary depending on the files included in the repository.

---

## 💡 Key Insights

The project demonstrates that demographic and lifestyle characteristics can provide useful predictive information for obesity-level classification.

Some of the major insights include:

* Weight is one of the strongest predictors of obesity level.
* Height contributes to differentiating between weight-status categories.
* Eating behavior has an important relationship with obesity classification.
* Physical activity is an important lifestyle-related factor.
* Family history of overweight provides additional predictive information.
* Machine learning models can achieve strong classification performance on this dataset.
* Logistic Regression provided a strong combination of performance and interpretability.

---

## ⚠️ Limitations

Despite the strong model performance, several limitations should be considered.

### Dataset Limitations

* The dataset contains only **2,111 observations**.
* The dataset may not fully represent the broader population.
* Some variables are self-reported and may contain reporting bias.
* The dataset may not capture all factors influencing obesity.
* External factors such as socioeconomic conditions, medical history, genetics, and environmental influences are not comprehensively represented.

### Machine Learning Limitations

A high test accuracy does not necessarily mean that the model will perform equally well on a different population.

Before applying such a model in a real-world healthcare setting, it would require:

* External validation
* Larger and more diverse datasets
* Clinical validation
* Bias and fairness assessment
* Careful interpretation by qualified professionals

---

## 🔮 Future Improvements

Several improvements could be explored in future versions of the project:

* Evaluate additional machine learning algorithms such as XGBoost and Gradient Boosting
* Perform more extensive feature engineering
* Use advanced hyperparameter optimization techniques
* Evaluate class-specific precision and recall
* Analyze confusion matrices in greater depth
* Apply explainable AI techniques such as SHAP
* Perform feature importance analysis
* Validate the model using an external dataset
* Increase dataset size and population diversity
* Develop an interactive prediction application using Streamlit
* Deploy the final model as an API

---

## 📌 Conclusion

This project demonstrates the development of a complete **end-to-end machine learning pipeline for obesity-level classification**.

After performing exploratory data analysis and preprocessing—including encoding, imputation, scaling, and feature preparation—multiple classification models were developed and optimized using **GridSearchCV and cross-validation**.

Logistic Regression achieved a **93.71% cross-validation accuracy**, while the final models achieved approximately **94% accuracy on the test dataset**.

The analysis identified **weight, height, eating behavior, physical activity, and family history of overweight** as important predictive factors.

Overall, the project demonstrates how machine learning can be applied to lifestyle and demographic data to identify patterns associated with different obesity levels. However, the limitations of the dataset mean that additional data, validation, and feature engineering would be required before considering real-world applications.

---

## 🎓 Academic Project

This project was completed as part of my **University Semester Project**.

The project allowed me to apply concepts from **machine learning, exploratory data analysis, data preprocessing, feature engineering, model optimization, cross-validation, and classification** to a real-world-style health and lifestyle dataset.

It also provided practical experience in building an **end-to-end machine learning pipeline**, from raw data exploration through model evaluation and interpretation.

---

## 👤 Author

Pavithra Gopinath


## 📚 Dataset Reference

**UCI Machine Learning Repository**

Estimation of Obesity Levels Based on Eating Habits and Physical Condition

https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition
