# BoardGames Data Mining — DM1

Data Mining project covering an end-to-end workflow for **board-game analytics**, from data preparation and exploratory analysis to clustering, classification, regression and association-rule mining.

## Project at a Glance

| Task | Methods | Best reported result |
|---|---|---|
| Clustering | K-Means, DBSCAN, Hierarchical Clustering | K-Means: **Silhouette 0.5794** with 3 clusters |
| Classification | Decision Tree, KNN, Naive Bayes | Decision Tree: **~70.9% test accuracy** |
| KNN classification | KNN tuning | **~62.39% accuracy** |
| Regression | Linear, Ridge, Lasso, Decision Tree, KNN | **R² ~0.557** |
| Pattern mining | Apriori association rules | Support, confidence and lift analysis |

## Objective

The project explores relationships between board-game characteristics and user ratings. It combines descriptive and predictive data-mining techniques to identify groups of similar games, classify rating levels, predict numeric ratings and discover frequent co-occurrence patterns.

## Analysis Workflow

### 1. Data Preparation and EDA

The source dataset is cleaned and transformed before modelling. The workflow includes:

- duplicate detection
- missing-value and invalid-value analysis
- removal of unnecessary attributes
- correlation analysis
- outlier analysis
- log transformation of highly skewed variables
- preparation of the final model-ready dataset

The main project notebook documents the broader exploratory and preprocessing workflow.

### 2. Clustering

Three unsupervised approaches are compared:

- **K-Means**
- **DBSCAN**
- **Hierarchical Clustering**

The strongest reported clustering configuration is K-Means with **3 clusters** and a **Silhouette Score of 0.5794**.

### 3. Classification

Ratings are converted into three categories:

- **Low**
- **Medium**
- **High**

The project evaluates Decision Tree, K-Nearest Neighbors and Gaussian Naive Bayes classifiers. Naive Bayes experiments additionally explore feature selection, SMOTE and PCA-based variants.

The tuned Decision Tree provides the strongest reported classification result at approximately **70.9% test accuracy**.

### 4. Regression

Numeric rating prediction is investigated with:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regression
- KNN Regression

Experiments compare feature configurations and model families using regression metrics. The strongest reported model reaches approximately **R² = 0.557**.

### 5. Association Rule Mining

The project applies the **Apriori algorithm** after discretizing continuous variables. Extracted rules are assessed using:

- support
- confidence
- lift

This complements the predictive models by identifying interpretable relationships among board-game characteristics.

## Repository Structure

```text
boardgames-data-mining/
├── data/
│   └── DM1_game_dataset_module.01.csv
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
├── report/
│   └── Project_Naeem_Nague_Sorce.pdf
├── .gitignore
└── README.md
```

## Notebook Guide

| Notebook | Purpose |
|---|---|
| `DM1_project.ipynb` | Main preprocessing and exploratory workflow |
| `k_means_01.ipynb` | K-Means clustering |
| `dbscan_Clustering.ipynb` | DBSCAN clustering |
| `Hierarchical_cluster.ipynb` | Hierarchical clustering |
| `DT_01.ipynb` | Decision Tree classification |
| `K-nn.ipynb` | KNN classification |
| `NB_baseline.ipynb` | Baseline Naive Bayes |
| `NB_all_methods.ipynb` | Extended Naive Bayes experiments |
| `Regression_DMipynb.ipynb` | Rating regression |
| `PM_02.ipynb` | Apriori / pattern mining |

## Technologies

Python, Jupyter Notebook, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Imbalanced-learn and Mlxtend.

## Reproducibility

The dataset required by the notebooks is included in `data/`. Open the relevant notebook in Jupyter or Colab and install the libraries imported by that notebook. Notebook checkpoints, virtual environments, local configuration and common secret files are excluded through `.gitignore`.

## Data Availability

The project dataset is included as `data/DM1_game_dataset_module.01.csv`. Users should respect the terms of the original data source when reusing or redistributing the data.

## Full Project Report

The complete methodology, experiments, figures, results and discussion are available in:

**[DM1 Project Report](report/Project_Naeem_Nague_Sorce.pdf)**

## Authors

- **Fiza Naeem**
- **Nague Ivane Maeva**
- **Lorena Sorce**

**University of Pisa — Data Mining project**
