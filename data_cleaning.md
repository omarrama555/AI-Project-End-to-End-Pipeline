# Data Cleaning

Data cleaning is a crucial step in the data analysis process. It involves identifying and correcting or removing errors and inconsistencies to improve the quality of data. Below is a detailed guide covering the most important aspects of data cleaning:

---

## 1. Missing Values

Missing values occur when no data is stored for a variable in an observation. They can be handled by:

- **Removing Missing Data**: Use methods like `dropna()` in pandas.
- **Imputing Missing Values**:
  - Mean/Median/Mode replacement
  - Interpolation for time series
  - Predictive models (e.g., KNN, Random Forest)
- **Retaining Missing Values**: Sometimes 'Unknown' is meaningful.

---

## 2. Duplicates

Duplicate entries may arise from data collection or merging datasets.

- **Identify Duplicates**: Use `duplicated()` in pandas.
- **Remove Duplicates**: Use `drop_duplicates()`.
- Always check whether duplicates are truly erroneous.

---

## 3. Outliers

Outliers are data points that deviate significantly from others.

- **Detecting Outliers**:
  - Statistical methods like IQR
  - Visual tools like boxplots or scatter plots
- **Handling Outliers**:
  - Remove if erroneous
  - Replace with mean/median or IQR bounds
  - Retain if justifiable

---

## 4. Wrong Data Types

Incorrect data types may hinder analysis.

- **Check types**: Use `.dtypes` in pandas.
- **Fix types**:
  - Convert strings to numbers: `astype(int)`, `pd.to_numeric()`
  - Convert strings to dates: `pd.to_datetime()`
  - Convert numbers to categories: `pd.cut()`

---

## 5. Text Normalization

Used to clean and standardize textual data.

- Convert to lowercase/uppercase
- Remove extra whitespace and special characters using regex
- Correct spelling errors (`textblob`)
- Standardize formats (e.g., phone numbers)
- Remove stop words

---

## General Steps

1. Explore data (`describe()`, `info()`)
2. Identify issues (missing, outliers, duplicates)
3. Plan cleaning strategy
4. Apply corrections
5. Validate results
6. Document changes

---

## Importance

- Increases accuracy and performance of models
- Reduces bias
- Saves time and cost
- Leads to reliable insights

---

## Tools

- **Python**: pandas, numpy, matplotlib, seaborn, textblob, re
- **R**: dplyr, tidyr, stringr, outliers, tm

---

> Data cleaning is iterative and depends on the context. Always document your changes.
