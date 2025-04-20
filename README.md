# 📊 Adult Dataset Profiling & Data Quality Analysis

This repository contains a comprehensive analysis of the **Adult Census Income Dataset**, including data profiling, data quality checks using **PyDeequ**, and schema validation with **Great Expectations**.

---

## 📁 Files

| File | Description |
|------|-------------|
| `Adult Dataset Profiling Report.pdf` | Auto-generated EDA report using YData Profiling |
| `DPDQ Homework.ipynb` | Python notebook used to clean, validate, and analyze the dataset |
| `Adult_Dataset_Assignment_Report.docx` | Final written report summarizing profiling and quality checks |

---

## 📦 Dataset Overview

- **Dataset**: [UCI Adult Dataset](https://archive.ics.uci.edu/ml/datasets/adult)
- **Goal**: Predict whether a person earns >$50K/year based on attributes like age, workclass, education, etc.
- **Observations**: 32,561
- **Features**: 15 (6 numeric, 9 categorical)

---

## 🧼 Steps Performed

### 1. 📋 Data Loading & Cleaning
- Handled missing values (`?`)
- Removed whitespaces
- Cast data types appropriately (e.g., age to integer)

### 2. 📈 Exploratory Data Analysis
- Used `ydata-profiling` for in-depth profiling
- Explored correlations, imbalances, and data distributions

### 3. ✅ Data Quality Validation
#### PyDeequ Checks:
- Column completeness
- Value constraints (e.g., income ∈ {`<=50K`, `>50K`})
- Uniqueness check (e.g., `fnlwgt`)

#### Great Expectations:
- Schema validation
- Uniqueness and category checks

---

## 🔎 Key Insights

- `fnlwgt` is not unique across rows.
- `capital-gain` and `capital-loss` are sparse (mostly 0).
- Minor completeness issues in `workclass`.
- No missing data (after cleaning).
- Imbalanced classes and categorical features.

---

## 📚 Technologies Used

- Python 3.12
- pandas, PySpark
- [YData Profiling](https://github.com/ydataai/ydata-profiling)
- [PyDeequ](https://github.com/awslabs/deequ)
- [Great Expectations](https://github.com/great-expectations/great_expectations)

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/your-username/adult-dataset-analysis.git
cd adult-dataset-analysis

# Install dependencies (example)
pip install pandas ydata-profiling great_expectations pyspark

# Open and run the notebook
jupyter notebook DPDQ_Homework.ipynb
