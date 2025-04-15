# Titanic: Machine Learning from Disaster – EDA & Predictive Modeling

This repository presents a complete analysis and prediction pipeline for the **Titanic: Machine Learning from Disaster** competition on [Kaggle](https://www.kaggle.com/competitions/titanic). The objective is to explore the data, engineer meaningful features, and build a predictive model that classifies passengers' survival outcomes.

---

## Table of Contents
- [Overview](#overview)
- [Notebook Features](#notebook-features)
- [Setup Instructions](#setup-instructions)
- [How to Generate Kaggle Submission](#how-to-generate-kaggle-submission)
- [Key Results](#key-results)
- [Next Steps](#next-steps)
- [Contact](#contact)
- [Notebook Features](#notebook-features)
- [Setup Instructions](#setup-instructions)
- [Key Results](#key-results)
- [Next Steps](#next-steps)

---

## Overview
This project includes:
- Structured data cleaning & preprocessing
- Feature engineering (`Title`, `FamilySize`, `IsAlone`, `HasCabin`)
- Detailed exploratory data analysis (EDA)
- Model development using Logistic Regression
- Export-ready prediction for Kaggle submission

---

## Notebook Features
| Section | Highlights |
|--------|------------|
| Dataset Overview | Summary of missing values, key fields, and data dimensions |
| Cleaning | Median imputation for `Age`, mode for `Embarked`, cabin flagging |
| Feature Engineering | Extracted titles, grouped rare ones, calculated family structure |
| EDA | Survival plots by class, gender, title, age & fare distributions |
| Modeling | Logistic Regression with `74.25%` validation accuracy |
| Export | `submission.csv` ready for Kaggle upload |

---

## Setup Instructions

1. Clone this repository or download the `.ipynb` file
2. Download the Titanic dataset from the [Kaggle competition page](https://www.kaggle.com/competitions/titanic/data)
3. Place `train.csv` and `test.csv` in the same folder as the notebook

### Install Required Libraries
```bash
pip install pandas numpy seaborn matplotlib scikit-learn
```

4. Open the notebook using Jupyter or Google Colab and run all cells

---

## How to Generate Kaggle Submission
At the end of the notebook:
```python
predictions = model.predict(X_test)
output = pd.DataFrame({"PassengerId": test_df["PassengerId"], "Survived": predictions})
output.to_csv("submission.csv", index=False)
```
Upload `submission.csv` to [Kaggle Submission Page](https://www.kaggle.com/competitions/titanic/submit)

---

## Key Results
- **Model Used**: Logistic Regression (Baseline)
- **Validation Accuracy**: `74.25%`
- **Key Predictors**: `Pclass`, `Title`, `FamilySize`, `IsAlone`, `Sex`

---
## Files in This Repository

| File Name | Description |
|-----------|-------------|
| `Titanic - Machine Learning from Disaster.ipynb` | Main Jupyter notebook with full workflow |
| `Titanic - Machine Learning from Disaster.html` | Web-rendered version of the notebook for easy viewing |
| `Titanic - Machine Learning from Disaster.pdf` | Printable/PDF version of the notebook |
| `submission.csv` | Kaggle-ready submission file generated from model predictions |

---

## Next Steps
- Add Random Forest and Gradient Boosting
- Implement cross-validation and grid search
- Tune thresholds and analyze confusion matrix

---

## Contact
Created by **Gaurav Tawri**  
📫 [Gauravtawri001@gmail.com](mailto:Gauravtawri001@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/gauravtawri)

---

📄 License: MIT
