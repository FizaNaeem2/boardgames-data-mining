# BoardGames Data Mining

Data mining analysis of a BoardGames dataset covering data preprocessing, clustering, classification, regression, and association rule mining.

## Project Overview

The project applies a complete data mining workflow to explore patterns in board game characteristics and predict game ratings.

The main stages of the project are:

- Data cleaning and preprocessing
- Exploratory data analysis
- Clustering
- Classification
- Regression
- Association rule mining

## Data Preprocessing

The dataset was cleaned and prepared before applying the data mining models. The preprocessing included:

- Duplicate detection
- Missing-value analysis
- Treatment of invalid and missing values
- Removal of unnecessary attributes
- Correlation analysis
- Outlier detection
- Log transformations for highly skewed variables
- Preparation of the final cleaned dataset

## Clustering

Three clustering approaches were explored:

- K-Means
- DBSCAN
- Hierarchical Clustering

K-Means produced the strongest clustering result with **3 clusters** and a **Silhouette Score of 0.5794**.

## Classification

Board game ratings were classified into three categories:

- Low
- Medium
- High

The following classification algorithms were evaluated:

### Decision Tree
The tuned Decision Tree achieved approximately **70.9% test accuracy**, providing the strongest classification performance.

### K-Nearest Neighbors (KNN)
The best tuned KNN model achieved approximately **62.39% accuracy**.

### Naive Bayes
Gaussian Naive Bayes was tested using baseline modelling as well as feature selection, SMOTE, and PCA approaches.

## Regression

Regression was used to predict board game ratings as a numeric target.

The following models were evaluated:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regression
- KNN Regression

The best model achieved an **R² of approximately 0.557**.

## Association Rule Mining

Association rule mining was performed using the **Apriori algorithm**.

Continuous variables were discretized before extracting frequent itemsets and association rules.

Rules were evaluated using:

- Support
- Confidence
- Lift

## Key Results

| Task | Best Result |
|---|---|
| Clustering | K-Means — Silhouette Score **0.5794** |
| Classification | Decision Tree — Accuracy **70.9%** |
| KNN Classification | Accuracy **62.39%** |
| Regression | Best R² **0.557** |
| Pattern Mining | Apriori Association Rules |

## Repository Structure

```text
boardgames-data-mining/
│
├── data/
│   └── Cleaned BoardGames dataset
│
├── notebooks/
│   ├── DM1_project.ipynb
│   ├── k_means_01.ipynb
│   ├── dbscan_Clustering.ipynb
│   ├── Hierarchical_cluster.ipynb
│   ├── DT_01.ipynb
│   ├── K-nn.ipynb
│   ├── NB_baseline.ipynb
│   ├── NB_all_methods.ipynb
│   ├── Regression_DMipynb.ipynb
│   └── PM_02.ipynb
│
├── report/
│   └── Project report
│
└── README.md
```

## Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- Mlxtend

## Project Report

The complete project report containing the methodology, experiments, visualizations, results, and discussion is available in the `report/` directory.
