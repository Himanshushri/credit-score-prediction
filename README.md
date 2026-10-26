
# Credit Score Prediction Using Machine Learning

## 📌 Project Overview

This project uses machine learning classification techniques to predict customer credit score categories based on financial and credit-related information.

The goal is to explore the dataset, preprocess the data, train classification models, and compare their performance to identify a suitable model for credit score prediction.

## 🎯 Objectives

* Explore and understand customer financial data.
* Clean the dataset and handle missing or placeholder values.
* Perform Exploratory Data Analysis (EDA) to identify patterns.
* Prepare numerical and categorical features for machine learning.
* Train and compare multiple classification models.
* Evaluate model performance using appropriate metrics.
* Examine feature importance and the impact of selected features.
* Save and reload the trained model for future predictions.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Google Colab
* Jupyter Notebook

## 🤖 Machine Learning Models

The notebook explores the following approaches:

* **Dummy Classifier:** Establishes a baseline for model comparison.
* **Random Forest Classifier:** Predicts credit score categories using an ensemble of decision trees.
* **Logistic Regression:** Provides a linear classification approach for comparison.

The models are compared using accuracy and macro F1-score.

## 🔍 Project Workflow

1. Load and inspect the dataset.
2. Clean missing values and placeholder entries.
3. Perform exploratory data analysis.
4. Prepare features and target labels.
5. Split the data by customer to reduce data leakage.
6. Build preprocessing pipelines.
7. Train and compare classification models.
8. Evaluate the selected model.
9. Analyze feature importance and perform sensitivity analysis.
10. Save, reload, and test the trained model.

## 📊 Evaluation

Model performance is assessed using:

* Accuracy
* Macro F1-score
* Classification report
* Confusion matrix
* Permutation feature importance

The notebook contains the detailed evaluation results.

## 📁 Repository Contents

* `Credit_Score_Prediction_Project_Submission.ipynb` — Complete project notebook.

## 🚀 How to Run

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Make the dataset available in your environment.
3. Update the dataset file path if necessary.
4. Install any missing dependencies.
5. Run the notebook cells in order.

**Note:** The original notebook uses Google Drive to load the dataset and save model artifacts. You may need to adjust the file paths when running it in a different environment.

## ⚠️ Limitations

* Model performance depends on the quality and representativeness of the dataset.
* Predictions should not be treated as definitive financial or lending decisions.
* Further testing, model tuning, and validation on independent data would be needed before any real-world deployment.

## 👨‍💻 Author

**Himanshu Shrivastava**

Computer Science Engineering Graduate | Aspiring AI/ML Practitioner

---

*This project was developed as part of an AI/ML internship project.*
