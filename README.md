# PCOS Diagnosis ML
Predicting Polycystic Ovary Syndrome from clinical indicators using machine learning in R

> Graduate coursework — University of Illinois Springfield, Machine Learning (CSC 534)

![R](https://img.shields.io/badge/R-RMarkdown-purple) ![ML](https://img.shields.io/badge/Domain-Clinical%20ML-green) ![Accuracy](https://img.shields.io/badge/Best%20Accuracy-97.5%25-brightgreen)

## Clinical context
PCOS affects an estimated 8–13% of people of reproductive age and is one of the most underdiagnosed endocrine conditions globally. Late or missed diagnosis is associated with increased risk of type 2 diabetes, cardiovascular disease, and infertility. This project builds and evaluates a suite of ML classifiers to identify high-risk patients from routine clinical measurements, supporting earlier, data-driven screening.

## Dataset
Kaggle PCOS Diagnosis Dataset — 1,000 patient records with five clinical features: Age, BMI, Menstrual Irregularity, Testosterone Level, and Antral Follicle Count. Target: PCOS Diagnosis (0 = No, 1 = Yes). Class imbalance addressed with SMOTE prior to model training.

## Methods
- **Exploration:** Histograms, boxplots, scatterplots, correlation analysis
- **Preprocessing:** Numeric feature scaling, SMOTE for class balancing
- **Models:** Logistic Regression (Lasso, Ridge, Elastic Net), Random Forest, Gradient Boosted Trees, SVM (Linear + Radial), Neural Network
- **Evaluation:** Accuracy, Kappa, Precision, Recall, F1, AUC-ROC

## Results
| Model | Accuracy | Kappa |
|---|---|---|
| SVM (Radial) | **97.5%** | **0.949** |
| Gradient Boosted Trees | — | — |
| Neural Network | High recall | Lower balance |

**Key finding:** Menstrual irregularity, BMI, and testosterone level were the strongest predictors. The SVM radial kernel achieved the best precision/recall balance. The neural network showed higher recall but lower overall consistency — a meaningful trade-off in clinical screening where false negatives carry real cost.

## Clinical significance
In screening settings, recall (sensitivity) often matters more than raw accuracy — a missed positive means a patient goes undiagnosed. This project explicitly evaluates that trade-off across models. Feature importance findings align with established clinical literature on PCOS risk factors, lending interpretability confidence to the outputs.

## Project structure
```
pcos-diagnosis-ml/
├── data/          # Kaggle PCOS dataset (CSV)
├── notebooks/     # pcos_analysis.Rmd — full analysis pipeline
├── report/        # PCOS_ML_Report.pdf
└── README.md
```

## How to run
```bash
git clone https://github.com/RachelRatajczak/pcos-diagnosis-ml.git
```
Open `notebooks/pcos_analysis.Rmd` in RStudio and knit to reproduce the full analysis.  
Dependencies: `caret`, `DMwR2`, `ggplot2`, `e1071`, `randomForest`, `gbm`, `nnet`

## References
1. Dalvi, S. (2025). PCOS diagnosis dataset. Kaggle.
2. World Health Organization. Polycystic Ovary Syndrome. WHO Fact Sheet, 2025.
3. Kim Kijun. PCOS Diagnosis ML Prediction with R. Kaggle, 2025.
