# Credit Score Prediction Using Machine Learning

A supervised machine-learning project that explores customer financial data and predicts one of three recorded credit-score categories: **Poor**, **Standard**, or **Good**.

> **Project scope:** The supplied brief used the title “Paisabazaar Banking Fraud Analysis,” but the dataset and target column describe credit-score categories, not a fraud label. This repository therefore focuses on **credit-score prediction**, not fraud detection.

## Project objectives

- Inspect the dataset and identify data-quality issues.
- Explore class balance and relationships among financial features.
- Prepare numerical and categorical features for modeling.
- Compare a majority-class baseline with Random Forest and Logistic Regression.
- Evaluate model performance with accuracy, macro F1, a classification report, and a confusion matrix.
- Examine the effect of `Credit_Mix` and estimate permutation feature importance.
- Save and reload the selected preprocessing-and-model pipeline.

## Notebook

[Open the complete project notebook](Credit_Score_Prediction_Project_Submission.ipynb).

The notebook contains the exploratory analysis, preprocessing, model training, evaluation, sensitivity check, feature-importance analysis, conclusion, and model-saving workflow.

## Tools and libraries

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- scikit-learn
- Joblib
- Google Colab / Jupyter Notebook

## Modeling workflow

1. **Data inspection and cleaning:** review columns, types, missing values, duplicates, and target distribution; convert known placeholder strings to missing values.
2. **Exploratory data analysis:** examine target balance, distributions, payment-delay patterns, `Credit_Mix`, numerical correlations, and income versus outstanding debt.
3. **Feature preparation:** predict `Credit_Score`; exclude identifiers and `Month`; omit `Type_of_Loan` because its combined text has many distinct values.
4. **Customer-level split:** use `GroupShuffleSplit` so records from one customer are not shared between training and test sets.
5. **Baseline and models:** compare a most-frequent `DummyClassifier`, a `RandomForestClassifier`, and `LogisticRegression`.
6. **Evaluation and interpretation:** compare accuracy and macro F1, inspect class-level metrics and confusion matrix, run a `Credit_Mix` sensitivity check, and calculate permutation importance.
7. **Save and reload:** save the complete selected pipeline and reports, then reload the pipeline and test it on held-out rows.

## Results

The notebook calculates the metrics from the current run and prints them in the model-comparison and conclusion sections. **Numerical scores are intentionally not reproduced here until they have been verified from a completed notebook run.** Refer to those outputs for the actual baseline, Random Forest, Logistic Regression, and selected-model results.

## Dataset and running the notebook

The notebook expects a file named `dataset-2.csv` at this Google Drive path:

```text
/content/drive/MyDrive/Credit_Score_Project/dataset-2.csv
```

To run it in Google Colab:

1. Open the notebook in Colab.
2. Make the dataset available at the path above, or change `file_path` to the location you use.
3. Run the cells in order from the beginning.
4. The notebook saves the model and CSV reports to the `Credit_Score_Project` folder in Google Drive.

The dataset is **not included in this repository**. Make sure you have permission to access and use it before attempting to reproduce the results. The notebook uses Google Colab's Drive integration, so a local Jupyter setup may require changes to the data and output paths.

## Important limitations

- Results are specific to this dataset and the customer-level train/test split; they do not establish production readiness.
- The source and prediction-time availability of `Credit_Mix` should be verified because the notebook explicitly checks how performance changes when it is removed.
- The age-below-18 cleaning rule is an assumption that should be confirmed against the data source.
- Further validation on an independent or later-period dataset, hyperparameter tuning, and fairness assessment would be needed before considering any real-world use.
- This is an educational credit-score classification project. It does **not** detect banking fraud and should not be used on its own for lending decisions.

## Author

**Himanshu Shrivastava**  
Computer Science Engineering | Aspiring AI/ML Practitioner

---

*Developed as part of an AI/ML internship project.*
