
# Crypto Clustering

## Overview

This project uses unsupervised machine learning techniques to cluster cryptocurrencies based on their market performance. The project aims to analyze whether cryptocurrencies are influenced by 24-hour and 7-day price changes, providing valuable insights into the grouping and characteristics of different cryptocurrencies.

### Key Techniques Used:
- **K-Means Clustering**: A popular unsupervised learning algorithm used for grouping the data into distinct clusters.
- **Principal Component Analysis (PCA)**: A dimensionality reduction technique to improve computational efficiency and enhance visualization.
- **Data Normalization**: Used to ensure that all features contribute equally to the analysis.

---

## Installation and Dependencies

### 1. Clone the repository:

```bash
git clone https://github.com/your-username/CryptoClustering.git
cd CryptoClustering
```

### 2. Install the required libraries:
Make sure you have the following libraries installed. You can install them by running:

```bash
pip install pandas hvplot scikit-learn matplotlib
```

### 3. Running the notebook:
Launch the notebook using Jupyter:

```bash
jupyter notebook Crypto_Clustering.ipynb
```

---

## Data Description

The dataset consists of cryptocurrency market data, specifically focusing on price percentage changes over a 24-hour and 7-day period. The data is preprocessed using the `StandardScaler` from `scikit-learn` to normalize the features before applying clustering algorithms.

- **Columns in the dataset**:
  - `price_change_percentage_24h`: 24-hour price percentage change.
  - `price_change_percentage_7d`: 7-day price percentage change.
  - Additional PCA components (`PC1`, `PC2`, `PC3`) after dimensionality reduction.

---

## Analysis and Methodology

### 1. Data Preprocessing
The cryptocurrency data was loaded and normalized using the `StandardScaler` module to ensure uniform scaling across features. The scaled data was then used to conduct clustering analysis.

### 2. K-Means Clustering
The K-Means algorithm was applied to group cryptocurrencies into clusters based on their price fluctuations. The **Elbow method** was used to determine the optimal number of clusters. After evaluating multiple `k` values, `k=4` was identified as the best option.

### 3. PCA for Dimensionality Reduction
Principal Component Analysis (PCA) was applied to reduce the dataset's dimensions while retaining approximately **89.5% of the original variance**. This not only improved computational performance but also made the data easier to visualize.

### 4. Elbow Curve Comparison
Elbow curves for both the original and PCA-transformed data were created, and they consistently showed that `k=4` is the optimal number of clusters for both datasets.

---

## Results

- **Cluster Visualization**: Cryptocurrencies were successfully grouped into four clusters, which were visualized in 2D space using PCA components. 
- **Inertia Comparison**: The clustering results were similar for both the original and PCA-reduced data, demonstrating that dimensionality reduction had minimal impact on the clustering performance.

---

## Key Insights

- **Cluster Behavior**: The clustering analysis revealed distinct patterns in cryptocurrency market behavior over 24-hour and 7-day periods. Cryptocurrencies with similar price movement tendencies were grouped into the same cluster.
- **PCA Efficiency**: PCA demonstrated that clustering could be achieved with minimal loss of information, improving processing efficiency.

---

## Future Work

- **Incorporating Additional Features**: More market indicators like trading volume or market capitalization could be included for a more robust clustering analysis.
- **Temporal Analysis**: Expanding the analysis over time to detect trends in cluster behavior.

---

## Conclusion

This project successfully demonstrated how unsupervised learning techniques like K-Means and PCA can be applied to analyze cryptocurrency market data. The analysis revealed valuable insights into how cryptocurrencies behave over different time periods, providing a foundation for further exploration in the cryptocurrency market.

## Additional Resources

- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [HvPlot Documentation](https://hvplot.holoviz.org/)
- [scikit-learn StandardScaler Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html)
- [scikit-learn PCA Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html)
- [scikit-learn K-Means Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
