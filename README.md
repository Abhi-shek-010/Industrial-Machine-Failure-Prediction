# Industrial Machine Failure Prediction

A machine learning project for predicting industrial equipment failures using the **AI4I 2020 Predictive Maintenance Dataset**.

> Project status: skeleton / in development

## Overview

This project explores predictive maintenance by using machine operating conditions and process measurements to identify whether a machine is likely to fail. The goal is to support earlier intervention, reduce unplanned downtime, and improve maintenance planning.

## Dataset

- **Name:** AI4I 2020 Predictive Maintenance Dataset
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset)
- **Target:** Machine failure (`Machine failure`)
- **Features:** Air temperature, process temperature, rotational speed, torque, tool wear, and product quality/type fields
- **Additional failure labels:** TWF, HDF, PWF, OSF, and RNF

Place the downloaded dataset in the data directory described below.

## Objectives

- Explore and clean the industrial sensor data.
- Analyze patterns associated with machine failures.
- Train one or more classification models.
- Evaluate performance with failure-focused metrics.
- Identify the most influential operating conditions.

## Planned Workflow

1. Load and inspect the dataset.
2. Handle missing values, duplicates, and irrelevant columns.
3. Explore class balance and feature relationships.
4. Split the data into training and test sets.
5. Apply preprocessing and address class imbalance where appropriate.
6. Train baseline and candidate classification models.
7. Evaluate predictions using precision, recall, F1-score, ROC-AUC, PR-AUC, and a confusion matrix.
8. Compare models and document findings.

## Project Structure

```text
.
├── data/
│   ├── raw/             # Original, unchanged dataset files
│   └── processed/       # Cleaned or transformed datasets
├── notebooks/           # Exploration and experiments
├── src/                 # Reusable data and modeling code
├── models/              # Saved model artifacts
├── reports/             # Figures, evaluation results, and summaries
├── requirements.txt     # Python dependencies
└── README.md
```

## Installation

```bash
git clone <repository-url>
cd Ind_flr_pred
python -m venv .venv
```

Activate the virtual environment:

```bash
# Windows PowerShell
.\.venv\Scripts\Activate.ps1

# macOS/Linux
source .venv/bin/activate
```

Install dependencies after `requirements.txt` has been added:

```bash
pip install -r requirements.txt
```

## Usage

Add project commands here as the implementation develops. For example:

```bash
python -m src.data_preparation
python -m src.train
python -m src.evaluate
```

Notebook workflow:

```bash
jupyter notebook notebooks/
```

## Models to Consider

- Logistic Regression as an interpretable baseline
- Decision Tree and Random Forest
- Gradient Boosting or XGBoost
- Support Vector Machine
- A calibrated classifier for failure-risk probabilities

Because failures are relatively uncommon, model selection should prioritize recall and PR-AUC alongside overall accuracy.

## Results

| Model | Precision | Recall | F1-score | ROC-AUC | PR-AUC |
|---|---:|---:|---:|---:|---:|
| Baseline | TBD | TBD | TBD | TBD | TBD |
| Best model | TBD | TBD | TBD | TBD | TBD |

## Reproducibility

- Record the Python version and dependency versions.
- Use a fixed random seed for repeatable experiments.
- Keep raw data unchanged and document preprocessing steps.
- Save evaluation configuration and model parameters with each experiment.

## Limitations

- The AI4I 2020 dataset is synthetic and may not represent every real industrial environment.
- The cost of false negatives and false positives should be defined with domain experts.
- Results may change when the model is evaluated on data from a different machine, site, or operating regime.

## Future Work

- Add feature engineering and time-aware data if operational histories become available.
- Tune decision thresholds according to maintenance costs.
- Add model explainability with feature importance or SHAP.
- Package the model as an API or monitoring dashboard.

## License

Add the project license here.

## Acknowledgements

This project uses the AI4I 2020 Predictive Maintenance Dataset provided through the UCI Machine Learning Repository.
