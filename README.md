# Predicting Online Enrollment U.S. Public Higher Education Institutions

Authors: Ying Sun, Zhonghan Xie, Soobin Jeon, Meng Wang

This project consists of three Jupyter notebooks that together examine institutional time-series patterns, online enrollment behavior, and the relationship between institutional characteristics, financial indicators, and cluster membership. The notebooks are designed to be read in sequence, as each builds conceptually on the previous analyses.

Github Repo: [https://github.com/meeewang/SI670_final_project](https://github.com/meeewang/SI670_final_project)

## Notebook 1: `final_01.ipynb`  
**Time Series Clustering of Institutions**

Explore time-series clustering of institutions using the `tslearn` package. The primary objectives are:

- To experiment with different distance metrics (e.g., Euclidean and DTW) and varying numbers of clusters in `TimeSeriesKMeans`.
- To assign cluster labels to institutions and merge the resulting cluster membership back into the original dataset.
- To generate descriptive statistics of institutional characteristics (e.g., size, sector, location, Carnegie classification) by cluster.

The output of this notebook provides the cluster definitions and descriptive context used in subsequent analyses.



## Notebook 2: `final_02.ipynb`  
**Predicting Online Enrollment Percentage**

Predict institutions’ online enrollment percentage using supervised machine learning models. Specifically, it:

- Implements four regression models: Interrupted Time Series Analysis, Random Forest, XGBoost, and LightGBM.
- Uses institutional characteristics and related predictors to model variation in online enrollment share.
- Further, we use Interrupted Time Series Analysis to model the online enrollment percentage and understand how different types of institutions respond to the COVID-19 pandemic in 2020.
- Compares model performance across algorithms using standard evaluation metrics.
- Identifies important predictors associated with higher or lower levels of online enrollment.

This notebook is independent of the clustering step and is intended to assess predictive performance and key correlates of online enrollment behavior.



## Notebook 3: `final_03.ipynb`  
**Predicting Cluster Membership Using Institutional Characteristics**

Examine whether institutional clusters identified in `final_01.ipynb` can be predicted using financial indicators and institutional characteristics. Specifically, it:

- To model cluster membership as an outcome using institutional financial variables and structural characteristics.
- To assess which features are most strongly associated with different cluster types.
- To evaluate the extent to which clusters reflect systematic institutional differences rather than purely time-series patterns.

**Important note on data differences:**  
The dataset used in this notebook differs from that in `final_01.ipynb`. Institutions with parent/child reporting relationships are excluded to ensure comparability and to avoid duplication or aggregation issues in the financial and institutional indicators used for prediction.



## Suggested Workflow

1. Start with `final_01.ipynb` to understand the construction and interpretation of institutional clusters.
2. Review `final_02.ipynb` to examine predictors of online enrollment percentage.
3. Use `final_03.ipynb` to explore how well institutional and financial characteristics explain cluster membership.


