# Coronary Artery Disease Prediction

A machine learning project predicting coronary artery disease diagnosis using clinical patient data and logistic regression with recursive feature elimination.

## Project Overview

This project develops a predictive model to identify patients at risk of coronary artery disease (CAD) based on clinical measurements and patient characteristics. The model achieved **91% accuracy** with strong performance across precision and recall metrics.

**Key Achievements:**
- 91% overall accuracy
- 89% recall (sensitivity)
- 92% precision
- Robust feature selection using RFECV
- Threshold optimization via AUC-ROC analysis

## Dataset

**Source:** Kaggle Heart Failure Prediction Dataset  
**Size:** 746 patients (after handling missing values)  
**Features:** Clinical measurements including age, blood pressure, cholesterol, heart rate, ECG results, and exercise test outcomes

**Target Variable:** Binary classification (CAD diagnosis: positive/negative)

## Methodology

### 1. Data Preprocessing
- Handled missing values (primarily cholesterol)
- Created categorical bins for continuous variables
- Applied MinMaxScaler for feature normalization
- Train-test split: 80-20

### 2. Feature Selection
Compared three approaches and selected **RFECV with continuous variables** for best performance.

### 3. Model Development
- **Algorithm:** Logistic Regression
- **Feature Selection:** RFECV
- **Threshold Optimization:** AUC-ROC curve analysis (optimized from 0.5 to 0.44)

## Results

| Metric | Score |
|--------|-------|
| Accuracy | 0.91 |
| Recall | 0.89 |
| Precision | 0.92 |
| F1 Score | 0.91 |
| Matthews Correlation Coefficient | 0.81 |

**Significant Predictors:** Age, sex, maximum heart rate, ST slope characteristics

## Technologies Used

- Python 3.x
- pandas, NumPy
- scikit-learn
- matplotlib, seaborn
- statsmodels

## Installation & Usage

```bash
pip install pandas numpy scikit-learn matplotlib seaborn statsmodels
jupyter notebook Group3_Stats_Main.ipynb
```

## Limitations & Future Work

- Small dataset size (746 observations) limits generalizability
- Recommend validation on larger, independent dataset
- Further investigation of counterintuitive coefficient patterns

## Course Context

**Course:** Statistics for Data Science  
**Institution:** University of Toronto / University of Waterloo (WatSPEED)  
**Term:** 2024  
**Grade:** A+ (98%)

---

**Note:** This model is for educational purposes only and should not be used for clinical diagnosis.
