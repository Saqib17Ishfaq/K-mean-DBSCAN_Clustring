Clustering Analysis with K-means and DBSCAN
This project applies unsupervised learning techniques — K-means and DBSCAN — to perform clustering on a dataset derived from a bank's marketing campaign. The aim is to explore natural groupings in the data and compare the performance of the two clustering algorithms using metrics like inertia and silhouette score.

📂 Dataset
File Used: bank-full.csv
The dataset contains customer-related features such as:
Age
Campaign duration
Economic indicators (euribor3m, emp.var.rate, etc.)
Missing values are handled, and only numerical features relevant to clustering are retained.

⚙️ Technologies Used
Python
Pandas, NumPy – Data manipulation
scikit-learn – ML models (KMeans, DBSCAN), preprocessing, metrics
Matplotlib – Visualizations
PCA – Dimensionality reduction for visualization

🔍 Workflow Overview
1. Data Preprocessing
Dropped or filled missing values.
Removed duplicates.
Selected relevant numeric features.
Standardized data using StandardScaler.

2. K-means Clustering
Evaluated optimal number of clusters using:
Elbow Method (based on inertia)
Silhouette Score
Performed clustering with:
k = optimal by silhouette
k = optimal by elbow
k = 3 (for comparison)
Visualized results using 2D PCA plots.
Analyzed cluster sizes and performance metrics.

3. DBSCAN Clustering
Selected subset of features for DBSCAN.
Used k-distance graph to estimate suitable eps value.
Performed DBSCAN clustering with eps=1.5 and min_samples=5.
Evaluated:
Number of clusters found
Number of noise (outlier) points
Silhouette score (if valid)
Visualized clusters using PCA.

4. Comparison
Compared:
K-means (silhouette-optimal)
K-means (elbow-optimal)
DBSCAN
Evaluated and visualized all models side-by-side to identify best clustering.

📊 Key Results
Algorithm	#Clusters	Silhouette Score	Outliers
K-means (Silhouette)	k=X	~0.XX	N/A
K-means (Elbow)	k=4	~0.XX	N/A
DBSCAN (eps=1.5)	Varies	~0.XX (if valid)	Yes
Note: Exact scores will vary depending on the dataset.

📌 Insights
K-means performs well with clearly separated, spherical clusters.
DBSCAN is useful for detecting arbitrary-shaped clusters and noise (outliers).
PCA visualization helps in comparing clustering quality visually.
Silhouette Score is a crucial metric for comparing clustering performance.

🚀 How to Run
Clone this repository.
Ensure bank-full.csv is in the project directory.
Install required libraries:
bash
pip install pandas numpy matplotlib scikit-learn
bash
python clustering_analysis.py
