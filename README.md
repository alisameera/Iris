# Iris Insights — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualisation-teal?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---

## Overview

Comprehensive EDA on the classic Iris dataset — 150 observations, 4 features, 3 species. Goes beyond basic visualisation to surface **which features actually separate the species**, detect and handle outliers, and draw conclusions relevant to downstream classification modelling.

---

## Dataset

| Attribute | Detail |
|-----------|--------|
| Rows | 150 |
| Features | 4 numerical + 1 categorical |
| Classes | Setosa · Versicolor · Virginica |
| Class balance | 50 observations each ✅ |
| Missing values | None |
| Duplicates | None |

---

## Key Findings

### Feature Separability
| Feature Pair | Separability | Notes |
|-------------|-------------|-------|
| **Petal length vs Petal width** | ⭐ Strongest | High correlation; best for classification |
| Petal length vs Sepal length | Good | Clear Setosa separation |
| Sepal length vs Sepal width | Weak | Significant species overlap |
| Sepal width alone | Weakest | Most overlap between species |

### Species Profiles
| Species | Petal Size | Sepal Size | Separability |
|---------|-----------|-----------|-------------|
| **Setosa** | Smallest | Small | Easily separated |
| **Versicolor** | Medium | Medium | Moderate overlap with Virginica |
| **Virginica** | Largest | Largest | Moderate overlap with Versicolor |

### Outliers
- **SepalWidthCm** contained outliers detected via IQR method
- Outliers removed to prevent distortion in downstream modelling
- All other features were relatively clean

### Correlations
- Petal length ↔ Petal width: **strong positive correlation** — as one increases, so does the other
- Petal dimensions are far more reliable classifiers than sepal dimensions

---

## Analysis Performed

- **Descriptive statistics** — mean, SD, min/max per feature and species
- **Univariate analysis** — histograms for each feature distribution
- **Bivariate analysis** — scatter plots and pairplots across species
- **Correlation heatmap** — numerical feature correlations
- **Outlier detection** — boxplots + IQR method
- **Outlier handling** — removal of flagged outliers

---

## Conclusion for Modelling

> **Petal length and petal width should be the primary features for any Iris classification model.** Sepal dimensions add noise rather than signal — particularly sepal width, which shows the most inter-species overlap. A classifier trained on petal dimensions alone would likely outperform one using all 4 features.

---

## Tech Stack

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Jupyter`

---

## Files

```
├── Iris_EDA.ipynb    ← main analysis notebook
├── iris.csv          ← dataset
└── README.md
```

---

## Author

**Sameera Ali** | [LinkedIn](https://www.linkedin.com/in/sameera-ali-0055252a2/) | [GitHub](https://github.com/alisameera)
