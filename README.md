# Project-Data-science-imp
MAIN 

# K-Means Clustering Analysis of London Tourism Data

##  Project Overview
This project applies **K-Means clustering** to segment international visitors to **London** based on their travel behavior, expenditure patterns, and stay duration. The analysis provides **valuable insights for tourism management, marketing strategies, and policy planning**.

##  Dataset Description
The dataset consists of international visitor records with key attributes:
- visits_000s: Number of visits (in thousands).
- spend_m: Total spending by visitors (in million pounds).
- nights_000s: Number of nights stayed (in thousands).

### Preprocessing Steps
- Handled Missing Values: Removed incomplete records to maintain data integrity.
- Outlier Detection & Treatment: Used IQR & Winsorization to handle extreme values.
- Feature Standardization: Applied StandardScaler to normalize numerical values.

##  Model Implementation

### 1 Determining the Optimal Clusters
- Used **Elbow Method** to identify the best `K` value.
- Silhouette Score & Davies-Bouldin Index confirmed **K = 3**.

### 2 Applying K-Means Clustering
- n_clusters = 3 (determined from Elbow Method).
- n_init = 10 (to ensure stability in centroid selection).
- Distance metric: Euclidean Distance.
- Assigned each visitor record to a **cluster based on travel behavior**.

### 3 PCA for Dimensionality Reduction
- Transformed data into **two principal components** to **visualize cluster separation**.
- The clusters were **clearly defined**, confirming effective segmentation.

### 4 Clustering Performance Metrics
| **Metric** | **Value** | **Interpretation** |
|------------|----------|--------------------------------|
|Silhouette Score | 0.5071 | Indicates well-separated clusters |
| Davies-Bouldin Index | 1.0219 | Lower value suggests better-defined clusters |
| Calinski-Harabasz Index| 79,685.37 | Higher value suggests distinct, compact clusters |

##  Insights from Clustering

### Cluster 0: Budget Travelers
- Short stays & low spending.
- Represents **students, backpackers, and short-term business travelers**.
- Focus on **budget-friendly tourism options**.

### Cluster 1: Frequent Spenders
- **Long stays & high spending**.
- Includes **luxury tourists, corporate executives, and long-term visitors**.
- Significant **economic contributors** to London tourism.

### Cluster 2: Mid-Term Visitors
- **Moderate spending & stay duration**.
- Represents **families, professionals, and regular visitors**.
- Key segment for **mid-range tourism services**.

##  Visualizations
 The following visualizations were generated:
1 **K-Means Cluster Size Distribution**  
2 **PCA-Based Cluster Representation**  
3 **Pair Plot of Features by Cluster**  


