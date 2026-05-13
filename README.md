# 🎓 Donor Prediction Model — Supervised & Unsupervised Learning

A machine learning project that predicts alumni donation behavior using a combination of supervised classification and unsupervised clustering techniques. Built with Python and Scikit-learn on real-world alumni data.

> **Completed under the guidance of Dr. Ming Lui**

---

## 📌 Project Overview

Universities and nonprofits spend significant resources on donor outreach. This project aims to identify which alumni are most likely to donate by building and comparing multiple machine learning models — helping organizations prioritize their efforts and reduce costs.

---

## 📂 Repository Structure

```
├── Final_Donar_Prediction.ipynb   # Main Jupyter Notebook
├── README.md                      # Project documentation
```

---

## 📊 Dataset

- **Source:** Alumni records (donor and non-donor CSVs)
- **Features used:**
  - Demographics: Age, Gender, Marital Status, Residence Type
  - Academic: College, Number of Degrees, First Graduation Year
  - Engagement: Events Attended, Athletics Count, Award Count, Fraternity/Sorority Count, Student Organization Count, Scholarship Count
- **Target:** `Donation` (1 = Donor, 0 = Non-Donor)
- **Balancing:** Non-donor records were undersampled to match donor count

---

## ⚙️ Workflow

### Part 1 — Data Loading & Preprocessing
- Loaded donor and non-donor CSV files
- Handled missing values and converted `Birthday` to `Age`
- Balanced the dataset using undersampling
- Applied log transformation on skewed features
- Scaled numerical features using MinMax Scaler
- One-hot encoded categorical variables
- Split into 80/20 train/test sets with stratification

### Part 2 — Exploratory Data Analysis (EDA)
- Distribution histograms of numerical features by donation status
- Correlation heatmap across all features
- Top 10 features most correlated with donation behavior

### Part 3 — Supervised Learning
Trained and evaluated 7 classifiers:

| Model | Notes |
|---|---|
| Logistic Regression | Baseline linear model |
| Random Forest | Ensemble of decision trees |
| Decision Tree | max_depth = 10 |
| K-Nearest Neighbors (KNN) | k = 7 |
| Gaussian Naive Bayes | Probabilistic classifier |
| AdaBoost | Boosting ensemble |
| Gradient Boosting | Best performing ensemble |

**Metrics tracked:** Accuracy, Precision, Recall, F1, F0.5, ROC-AUC, Train Time, Predict Time

### Part 4 — Unsupervised Learning
- PCA for dimensionality reduction before clustering
- **K-Means:** Elbow method + Silhouette analysis to find optimal k; cluster profiles compared against actual donor labels
- **DBSCAN:** K-distance plot for eps selection; noise detection and cluster visualization

### Part 5 — Model Comparison & Final Summary
- Side-by-side bar charts comparing Accuracy, F1, and ROC-AUC across all supervised models
- Unsupervised results compared using Silhouette Score, Adjusted Rand Index (ARI), and Normalized Mutual Information (NMI)

---

## 🛠️ Technologies Used

- **Language:** Python 3
- **Libraries:**
  - `pandas`, `numpy` — Data manipulation
  - `matplotlib`, `seaborn` — Visualization
  - `scikit-learn` — Machine learning models & metrics

---



## Acknowledgements

Special thanks to **Dr. Ming Lui** for his guidance and mentorship throughout this project.

---

## 📄 License

This project is for academic and educational purposes.
