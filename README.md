# PCOS Diagnosis Machine Learning

This project uses machine learning to predict Polycystic Ovary Syndrome (PCOS) based on common patient risk factors. The goal is to identify key indicators and provide predictive tools to aid early diagnosis.

## Dataset

The dataset comes from Kaggle: [PCOS Diagnosis Dataset](https://www.kaggle.com/datasets/samikshadalvi/pcos-diagnosis-dataset).  
It contains 1000 entries with five main features: Age, BMI, Menstrual Irregularity, Testosterone Level, and Antral Follicle Count. The target variable is **PCOS Diagnosis** (0 = No, 1 = Yes).

## Project Structure

- data/ ← CSV dataset
- notebooks/ ← R Markdown file with analysis, modeling, and plots
- figures/ ← Visualizations exported from analysis
- report/ ← PDF of the full project report
- README.md ← This file


## Methods
- **Data Exploration & Visualization:** Histograms, boxplots, scatterplots, correlation analysis
- **Preprocessing:** Scaling numeric features, SMOTE for balancing classes
- **Models Trained:** Logistic Regression (Lasso, Ridge, Elastic Net), Random Forest, Gradient Boosted Trees, Support Vector Machine (Linear & Radial), Neural Network
- **Evaluation Metrics:** Accuracy, Kappa, Precision, Recall, F1-score, AUC-ROC

## Key Findings
- **Best Model:** SVM with radial kernel (Accuracy: 97.49%, Kappa: 0.949)  
- **Important Features:** Menstrual irregularity, BMI, testosterone level, antral follicle count  
- Neural network showed slightly higher recall but lower overall balance  

## How to Use
1. Clone the repository:
```bash
git clone https://github.com/RachelRatajczak/pcos-diagnosis-ml.git
2. Open the notebooks/pcos_analysis.Rmd in RStudio to explore the analysis and run the code.
3. View the full report in report/PCOS_ML_Report.pdf.

References

1. Dalvi, S. (2025). PCOS diagnosis dataset. Kaggle.

2. World Health Organization. Polycystic Ovary Syndrome. WHO Fact Sheet, 2025.

3. Kim Kijun. PCOS Diagnosis ML Prediction with R. Kaggle, 2025.
