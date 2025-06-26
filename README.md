# Cluster-analysis-of-epigenome

## Project Description

This project explores the application of various clustering techniques (KMeans, DBSCAN, Hierarchical Clustering, GMM, and Spectral Clustering) to epigenomic data from high-grade serous ovarian carcinoma. The clustering was performed at two levels:

 - Individual CpG Loci

 - Regions defined by Sliding Windows

The goal is to discover potentially significant methylation patterns that can point to distinct epigenomic signatures and potentially aid in early diagnosis or therapy strategies.

## Technologies and Libraries

The analysis is implemented in Python (version ≥ 3.9) within the Jupyter Notebook environment.

Required libraries: numpy, pandas, scikit-learn, scipy, matplotlib, seaborn, kneed, collections, mpl_toolkits

Installation:
```bash
pip3 install numpy pandas scikit-learn scipy matplotlib seaborn kneed

```

## Directory and File Descriptions

The data/ directory contains the following files:

 - rows-with-nan.csv: All rows from the original dataset that contain at least one NaN in Beta_value columns.
 - unfiltered-df.csv: The dataset after removing rows with NaN Beta_values and redundant columns.
 - filtered-df.csv: The dataset of CpG sites with significant methylation variation.
 - beta-values.csv: Extracted Beta_value columns from filtered-df.csv (used for CpG site clustering).
 - regions_df.csv: Dataset representing sliding windows of CpG sites, including calculated average correlations.
 - regions_df_clusters.csv: The sliding window dataset augmented with hierarchical clustering labels.

## Usage
1. Clone the repository.
2. Install required libraries:
```bash
pip3 install numpy pandas scikit-learn scipy matplotlib seaborn kneed

```
3. Open the .ipynb notebook in Jupyter.
4. Run the notebook sequentially to review the data preprocessing, clustering, and visualizations.

## Results and Conclusions

The results indicate that:
- Clustering CpG regions using sliding windows provides much clearer and robust clustering compared to clustering individual CpG sites.
- Hierarchical clustering performed best for sliding window data, suggesting the presence of natural epigenomic groupings across the genome.
- The outcomes support the use of regional (window-based) epigenomic analyses as an effective approach for identifying epigenomic signatures in high-grade serous ovarian carcinoma.

