# Intelligent Predictive Maintenance - Machine Failure Risk Management

A machine learning project focused on predicting machine failure risk and supporting proactive maintenance decisions in industrial environments. The project analyzes equipment operating data to identify failure-prone assets before breakdowns occur, helping reduce downtime and maintenance costs.

## Project Overview

Unexpected equipment failures can cause production losses, safety risks, and expensive downtime. This project applies data-driven predictive analytics to estimate the probability of machine failure using historical sensor and operational data.

The workflow includes:
- data preprocessing and exploratory analysis
- feature engineering and model comparison
- model evaluation using classification metrics
- selection of a threshold suitable for maintenance decision-making
- documentation of results in a final technical report

## Objectives

- predict whether a machine is likely to fail in the near future
- compare multiple machine learning models for predictive maintenance
- optimize model performance for business-critical recall and actionability
- support preventive maintenance planning with interpretable model results

## Repository Contents

- `Predictive_Maintenance.ipynb` — main notebook containing data analysis, modeling, and evaluation
- `Final_Technical_Report.pdf` — technical documentation describing the methodology and findings
- `model_comparison.csv` — summary of model performance across multiple classifiers
- `experiment_results.csv` — hyperparameter tuning and validation performance results

## Dataset

This project uses the AI4I 2020 Predictive Maintenance Dataset, which is publicly available from the UCI Machine Learning Repository:

https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset

The dataset contains simulated industrial sensor and maintenance records used to model machine health and predict failure events. It includes operational variables such as air temperature, process temperature, rotational speed, torque, tool wear, and machine failure indicators. This benchmark dataset is widely used for predictive maintenance and reliability analysis research.

## Methodology

1. Data loading and inspection
2. Exploratory data analysis (EDA)
3. Data cleaning and preprocessing
4. Feature preparation for supervised learning
5. Training and comparing multiple classifiers:
   - Logistic Regression
   - Random Forest
   - Artificial Neural Network (ANN)
6. Evaluation using accuracy, precision, recall, F1-score, ROC-AUC, and PR-AUC
7. Threshold tuning for practical maintenance decisions
8. Reporting of business-oriented model selection based on risk and cost trade-offs

## Model Comparison Results

The following results summarize the model performance reported in `model_comparison.csv`:

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC | PR-AUC |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Logistic Regression | 0.9193 | 0.2635 | 0.7647 | 0.3920 | 0.9031 | 0.3823 |
| Random Forest | 0.9533 | 0.4112 | 0.8627 | 0.5570 | 0.9725 | 0.8450 |
| ANN | 0.9653 | 0.4938 | 0.7843 | 0.6061 | 0.9705 | 0.7048 |

From the reported comparison, the Random Forest model provided a strong balance between predictive performance and business cost efficiency, while ANN achieved the highest overall accuracy. The final model choice depends on the priority between maximized detection performance and cost-sensitive decision thresholds.

## Key Takeaways

- Predictive maintenance can be framed as a binary classification problem for early failure detection.
- Recall is highly important in this domain because missing a true failure is often more costly than a false alarm.
- Model threshold tuning is essential when translating prediction probabilities into maintenance actions.
- Data-driven maintenance planning can reduce downtime and improve asset reliability.

## Tech Stack

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Pinnamaneni-Annapurna25/Intelligent-Predictive-Maintenance-Machine-Failure-Risk-Management.git
cd Intelligent-Predictive-Maintenance-Machine-Failure-Risk-Management
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate
# On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter
```

### 4. Open the notebook

```bash
jupyter notebook Predictive_Maintenance.ipynb
```

## Usage

Run the notebook cells in order to:
- load the dataset
- explore the data and feature distributions
- preprocess the variables
- train the candidate models
- evaluate predictive performance
- compare results and determine the recommended operating threshold
- review the final conclusions for maintenance actions

## Project Goal

The primary goal of this project is to reduce unexpected machine downtime by identifying failure-prone equipment early using machine learning and risk-based maintenance strategies.

## License

This project is intended for educational and research use.

## Contact

For questions or collaboration opportunities, please open an issue in this repository or contact the project owner through the GitHub profile associated with the repository.
