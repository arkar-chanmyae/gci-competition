# 🏦 Home Credit Default Risk — Machine Learning Competition

This repository contains the machine learning pipeline and exploratory data analysis for the **GCI Global 2026 Home Credit Default Risk Competition**.

## 📌 Problem Overview
The objective is to predict whether a loan applicant is likely to default on their loan (`TARGET = 1` for default / payment difficulties, `TARGET = 0` for repayment) based on historical application attributes, demographic details, and financial indicators.

- **Target Metric**: Area Under the ROC Curve (ROC AUC) / Predicted default probability
- **Target Variable**: `TARGET` (Binary classification)

## 📁 Repository Structure
```
gci-competition/
├── competition.ipynb                  # Main experimentation & model training notebook
├── tutorial.ipynb                     # Baseline tutorial notebook
├── HomeCredit_columns_description.xlsx# Feature descriptions
├── README.ipynb                       # Competition guidelines notebook
├── README.md                          # Repository documentation
├── input/                             # [Ignored in Git] Raw dataset files
│   ├── train.csv                      # Training set with ground truth TARGET
│   ├── test.csv                       # Test set for submission evaluation
│   └── sample_submission.csv          # Submission format template
└── output/                            # [Ignored in Git] Model checkpoints & submission CSVs
    └── submission.csv
```

## 🛠️ Getting Started

### 1. Prerequisites & Virtual Environment
Ensure Python 3.10+ is installed. Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install numpy pandas scikit-learn matplotlib seaborn lightgbm xgboost jupyter
```

### 2. Dataset Setup
Because training and test CSV files exceed recommended Git repository file sizes, they are excluded via `.gitignore`.
Place the datasets inside the `input/` directory:
- `input/train.csv`
- `input/test.csv`
- `input/sample_submission.csv`

### 3. Running the Pipeline
Launch Jupyter Notebook or JupyterLab:
```bash
jupyter notebook competition.ipynb
```
Follow the pipeline steps:
1. **EDA & Data Understanding:** Distribution analysis, correlation matrices, and missing value profiling.
2. **Preprocessing & Feature Engineering:** Imputation strategies, categorical encoding, handling skewed distributions.
3. **Model Training & Cross-Validation:** Baseline Logistic Regression, Tree Ensembles (Random Forest / LightGBM / XGBoost).
4. **Inference & Submission:** Generating calibrated probabilities outputted to `output/submission.csv`.

---
*Created as part of GCI Global 2026.*
