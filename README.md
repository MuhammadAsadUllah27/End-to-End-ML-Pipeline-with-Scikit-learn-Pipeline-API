# End-to-End ML Pipeline with Scikit-learn Pipeline API

##  Objective of the Task

The objective of this project is to develop a **robust and reusable machine learning pipeline** to predict customer churn in a telecom dataset. Customer churn refers to the likelihood of a customer leaving a service.

This project aims to:

* Automate data preprocessing and transformation
* Train multiple machine learning models
* Perform hyperparameter tuning for optimal performance
* Evaluate models using appropriate metrics
* Build a production-ready pipeline that can be reused for future predictions

---

##   Methodology / Approach

### 1. Data Loading

* The dataset is divided into:

  * `churn-bigml-80.csv` (training data)
  * `churn-bigml-20.csv` (testing data)
* Data is loaded using **Pandas**

### 2. Data Preprocessing

* Features and target variable (`Churn`) are separated
* Data types are identified:

  * Numerical features
  * Categorical features
* Preprocessing steps:

  * Missing value handling:

    * Numerical → Median imputation
    * Categorical → Most frequent imputation
  * Feature scaling using **StandardScaler**
  * Categorical encoding using **OneHotEncoder**
* All preprocessing steps are combined using **ColumnTransformer** inside a **Pipeline**

### 3. Model Development

* Two machine learning models are used:

  * Logistic Regression (baseline model)
  * Random Forest Classifier (ensemble model)
* A unified **Scikit-learn Pipeline** is created that includes:

  * Preprocessing
  * Model training

### 4. Hyperparameter Tuning

* **GridSearchCV** is applied to:

  * Explore multiple parameter combinations
  * Select the best-performing model automatically

### 5. Model Evaluation

The model is evaluated using:

* Accuracy Score
* Precision, Recall, and F1-score (Classification Report)
* Confusion Matrix
* ROC-AUC Score

### 6. Model Export

* The final optimized pipeline is saved using **joblib**
* This allows easy reuse in production environments

---

##   Key Results / Observations

* The machine learning pipeline successfully automated the entire workflow from preprocessing to prediction
* **Random Forest** generally performed better than Logistic Regression due to its ability to capture complex patterns
* The use of **GridSearchCV** significantly improved model performance by selecting optimal hyperparameters
* Evaluation metrics such as **F1-score and ROC-AUC** provided better insight than accuracy alone, especially for imbalanced data
* The pipeline ensures:

  * Consistency in preprocessing
  * Reproducibility of results
  * Ease of deployment

###   Insight

The model can effectively identify customers likely to churn, enabling businesses to take proactive actions such as targeted marketing or improved customer service to reduce churn rates.

---

##   Conclusion

This project demonstrates how to build a **production-ready machine learning pipeline** using Scikit-learn. The approach ensures scalability, reusability, and reliability, making it suitable for real-world applications.

---
