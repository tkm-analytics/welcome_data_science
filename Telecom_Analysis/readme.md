# Hyper-Parameter Tuning Exercise

## Overview
This project explores the impact of different hyper-parameters on data visualization, clustering, and feature selection. The exercise uses a telecom churn dataset to evaluate how hyper-parameter choices influence analysis conclusions. Three key hyper-parameters are investigated:

### 1. T-SNE Perplexity (Visualization)
- **What it does:** Controls how the algorithm balances attention between local and global structure.
- **Why it matters:** Different perplexity values produce very different visual representations of data clusters.

### 2. Number of Principal Components (PCA) for Clustering (Clustering)
- **What it does:** Determines how many dimensions from PCA are retained for clustering.
- **Why it matters:** The number of retained components affects cluster separability and clustering quality.

### 3. Number of Clusters for Unsupervised Feature Selection (Feature Selection)
- **What it does:** Determines how many clusters are formed when evaluating feature importance.
- **Why it matters:** Different cluster counts lead to different features being selected and impact downstream classification accuracy.

---

## Dataset
- **Name:** Telecom Churn Dataset
- **File:** telecom_churn.csv
- **Description:** Customer data with features describing their service usage, account details, and whether they churned.

---

## Analysis Workflow
1. **Preprocessing:**
   - Encode categorical variables.
   - Standardize numerical features.

2. **T-SNE Visualization:**
   - Test perplexity values of 5, 30, and 100.
   - Visualize customer clusters under each setting.

3. **Clustering with PCA:**
   - Perform PCA with varying number of components (5, 20, 50, 100).
   - Evaluate cluster quality (Silhouette Score).

4. **Unsupervised Feature Selection:**
   - Apply KMeans clustering with 2, 3, 5, and 10 clusters.
   - Use cluster means to identify top features.
   - Train logistic regression on these selected features.
   - Evaluate classification accuracy.


---

## Key Findings
| Parameter | Impact on Results |
|---|---|
| **T-SNE Perplexity** | Higher perplexity captures global structure, lower focuses on local clusters. |
| **Number of PCs** | Too few components limit cluster separation; too many can introduce noise. |
| **Number of Clusters (Feature Selection)** | More clusters allow finer feature importance granularity, but risk overfitting. |

---

## How to Run
1. Load `telecom_churn.csv` into the same directory.
2. Run the provided notebook `hp_tuning.ipynb`.
3. Inspect the visualizations and accuracy reports.

---

## Dependencies
- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

---

## Conclusion
Careful tuning of these hyper-parameters significantly influences conclusions drawn from the data. Properly balancing visualization clarity, clustering separability, and feature selection quality is essential to produce reliable downstream models.

---

## Author
This analysis was developed as part of a comprehensive hyper-parameter tuning exercise in computational applications in statistics.

