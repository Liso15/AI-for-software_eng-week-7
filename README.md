# AI-for-software_eng-week-7

## COMPAS Fairness Analysis Project

This project explores algorithmic fairness in criminal justice risk assessment using the COMPAS dataset and the AIF360 toolkit. The goal is to analyze and mitigate racial bias in recidivism predictions, focusing on the disparity between African-American and Caucasian groups.

### Dataset
- **Source:** `compas-scores-two-years.csv`
- **Description:** Contains demographic, criminal history, and COMPAS risk scores for defendants, including the `two_year_recid` outcome and `race` as a protected attribute.

### Methodology
1. **Data Cleaning:**
   - Filter the dataset to include only African-American and Caucasian individuals with valid recidivism labels.
   - Remove rows with missing values in key columns.
2. **Fairness Analysis:**
   - Use AIF360's `StandardDataset` to structure the data for fairness metrics.
   - Define privileged (`Caucasian`) and unprivileged (`African-American`) groups.
   - Calculate False Positive Rates (FPR) for both groups using AIF360's `ClassificationMetric`.
   - Visualize disparities in FPR using bar plots.
3. **Bias Mitigation:**
   - Apply the Reweighing algorithm to adjust sample weights and reduce bias.
   - Recalculate and visualize FPR after mitigation.

### How to Run
1. **Install dependencies:**
   - Python 3.7+
   - Install required packages:
     ```bash
     pip install numpy pandas matplotlib aif360
     ```
2. **Run the notebook:**
   - Open `Firness_Analysis.ipynb` in Jupyter Notebook or VSCode.
   - Execute cells sequentially to reproduce the analysis and plots.

### Main Files
- `compas-scores-two-years.csv`: The dataset used for analysis.
- `Firness_Analysis.ipynb`: The main analysis notebook.

### Results
- The notebook demonstrates how to measure and visualize racial disparities in risk assessment, and how reweighing can help mitigate bias.

---

