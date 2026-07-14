# Customer-Segmentation-Using-Unsupervised-Learning
Cluster customers based on spending habits and propose marketing strategies tailored to each segment. 

#Contents
- `Customer_Segmentation_Mall_Customers.ipynb` — full analysis notebook (EDA → K-Means → PCA/t-SNE → strategy)

## Dataset
This notebook expects **`Mall_Customers.csv`** (the "Mall Customer Segmentation Data" dataset, 200 rows:
`CustomerID`, `Gender`, `Age`, `Annual Income (k$)`, `Spending Score (1-100)`) in the same folder.

Download it from Kaggle (search "Mall Customer Segmentation Data") and place the CSV next to the
Notebook before running.

> If the CSV is missing, the notebook automatically generates a synthetic placeholder dataset with the
> same schema so it still runs end-to-end for demonstration — replace it with the real file for your
> final submission/grading.

## How to run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook Customer_Segmentation_Mall_Customers.ipynb
```

## Summary of approach
1. **EDA** — inspect structure, missing values, distributions, and correlations.
2. **Feature scaling** — standardize Age, Annual Income, and Spending Score.
3. **K-Means** — determine optimal k via Elbow Method + Silhouette Score, then fit final model.
4. **Cluster profiling** — compute per-cluster averages to characterize each segment.
5. **PCA & t-SNE** — reduce to 2D to visually validate cluster separation.
6. **Marketing strategy** — map each segment (e.g., high income/high spend, low income/high spend) to a
   tailored marketing recommendation.
