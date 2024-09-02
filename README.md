# Cryptocurrency Market Clustering with K-Means and PCA

## Overview

This project performs clustering analysis on cryptocurrency market data to identify distinct groups based on various performance metrics. Using K-Means clustering and Principal Component Analysis (PCA), the project aims to find the optimal number of clusters and visualize the results.

## Key Components

1. **Data Preprocessing**:
   - Load and clean the cryptocurrency market data.
   - Normalize the data using `StandardScaler`.

2. **K-Means Clustering**:
   - Determine the optimal number of clusters (k) using the Elbow method.
   - Perform K-Means clustering with the optimal k.

3. **Principal Component Analysis (PCA)**:
   - Reduce the data to three principal components.
   - Determine the explained variance of the principal components.

4. **Visualization**:
   - Visualize the clusters using scatter plots.
   - Compare clustering results with and without PCA optimization.

## Data Preprocessing

- Load the data from `crypto_market_data.csv`.
- Normalize the data using `StandardScaler`.
- Inspect the data to ensure it has been loaded and scaled correctly.

## K-Means Clustering

1. **Elbow Method**:
   - Compute the inertia for k values from 1 to 11.
   - Plot the Elbow curve to identify the optimal k.

2. **Fit K-Means Model**:
   - Perform K-Means clustering with the identified optimal k (k=3).
   - Predict the cluster for each cryptocurrency.

3. **Visualization**:
   - Create scatter plots to visualize the clusters.
   - Hover over points to identify specific cryptocurrencies.

## Principal Component Analysis (PCA)

1. **PCA Transformation**:
   - Reduce the data to three principal components.
   - Calculate the explained variance (0.895, indicating high retention of information).

2. **Elbow Method with PCA**:
   - Compute the inertia for k values from 1 to 11 on PCA-reduced data.
   - Plot the Elbow curve to identify the optimal k.

3. **Fit K-Means Model with PCA**:
   - Perform K-Means clustering on the PCA-reduced data with the identified optimal k (k=3).
   - Predict the cluster for each cryptocurrency.

4. **Visualization**:
   - Create scatter plots to visualize the PCA-reduced clusters.
   - Hover over points to identify specific cryptocurrencies.

## Results and Analysis

- The optimal number of clusters (k) identified is 3, both with and without PCA.
- Clustering with PCA showed similar cluster quality but with improved computational efficiency and visualization clarity.
- PCA retained ~89.5% of the information with just three components.

## Quick Start

1. **Install Required Packages**:
   - `pandas`, `hvplot`, `sklearn`
2. **Run the Analysis**:
   - Load and preprocess the data.
   - Perform K-Means clustering.
   - Apply PCA for dimensionality reduction.
   - Visualize and interpret the results.

## Key Findings

- **Optimal Clustering**: k=3 provides a good balance of cluster separation and computational efficiency.
- **PCA Benefits**: Reducing features via PCA improves clustering efficiency and visualization while retaining most of the data's variability.

## Future Work

- Experiment with different clustering algorithms (e.g., DBSCAN, Hierarchical Clustering).
- Use additional features or external data to enhance clustering insights.
- Implement real-time clustering and analysis for dynamic market data.

For detailed implementation and full analysis, refer to the source code and accompanying notebooks.
