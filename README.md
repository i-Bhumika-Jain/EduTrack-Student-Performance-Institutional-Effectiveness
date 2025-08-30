# EduTrack — Student Performance Analysis

A lightweight exploratory data analysis (EDA) project around the classic StudentsPerformance dataset, focused on understanding how factors such as gender, parental education, lunch type, and test preparation relate to exam scores (Math, Reading, Writing). The work is implemented in a single Jupyter notebook and produces a cleaned CSV for reuse.

---

## What’s we have done

- Data loading from StudentsPerformance.csv.
- Basic data health checks (shape, info, missing values, duplicates count).
- Cleaning & standardization
- Normalized column names to consistent identifiers.
- Standardized categorical values (lower-cased, trimmed).
- Dropped rows with missing values.
- Exploratory analysis & visualizations
- Average subject scores by Gender.
- Average subject scores by Parental Education.
- Distribution of Math scores by Gender and Race/Ethnicity.
- Distribution of Math by Lunch Type (violin plot).
- Overall averages & variances across Math, Reading, Writing.
- Statistical tests
- Two-sample t-tests for gender differences across subjects.
- Correlation of parental education (ordinal-encoded) with scores.
- T-test on test prep vs. math scores.
- Chi-square test for association between lunch type and test prep.
- Output
- Cleaned dataset saved as StudentsPerformance_Cleaned.csv.

---


Data & analysis
- Explicitly handle duplicates (currently counted but not dropped).
- Validate score ranges (0–100) and clip/flag outliers if needed.
- Add a brief data dictionary describing each column after cleaning.
- Consider modeling tasks:
- Regression: predict average score / subject score from demographics & prep.
- Classification: flag “at-risk” students by threshold.
- Include cross-validation, feature importance, and fairness checks.

Quality checks
- Add unit tests for cleaning/encoding helpers (e.g., pytest).
- Add a pre-commit setup (black, isort, flake8/ruff, nbstripout).

---

## Getting started

### 1) Prerequisites
- Python 3.9+ (3.10+ recommended)

### 2) Install dependencies
You can either install directly:

pip install -r requirements.txt


or install individually:

pip install numpy pandas matplotlib seaborn scipy jupyterlab


Suggested requirements.txt:
numpy>=1.26
pandas>=2.2
matplotlib>=3.8
seaborn>=0.13
scipy>=1.11
jupyterlab>=4.0


### 3) Get the dataset
Placed StudentsPerformance.csv same repo file 

### 4) Run the notebook
jupyter lab

Open EduTrack (1).ipynb and run all cells. A cleaned file named StudentsPerformance_Cleaned.csv will be produced.

---

## Key findings (from the current analysis)

- Gender differences: Males tend to score higher in Math, while females generally outperform in Reading/Writing.
- Parental education shows a positive correlation with scores across subjects.
- Test preparation completion is associated with higher average scores.
- Lunch type differences suggest potential socioeconomic effects on performance/preparation.
 These are aggregate-level insights; consider deeper segmentation and fairness checks before making policy/academic decisions.
---


## Acknowledgments
- Dataset: “Students Performance in Exams” (commonly found on Kaggle on https://www.kaggle.com/datasets/spscientist/students-performance-in-exams) 
