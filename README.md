# breast-cancer-survival-prediction
Predicting 5-year breast cancer survival using clinical and genomic data. This R-based project explores the impact of hormone receptors (ER, PR, HER2) and applies LDA, PCA-KNN, and clustering methods to improve classification accuracy for distant metastasis outcomes.

Project Overview
Breast cancer is one of the most common cancers worldwide, primarily affecting women. Accurate prognosis plays a crucial role in planning effective treatment strategies. This analysis is based on a dataset of 295 patients treated at the Netherlands Cancer Institute, with a goal to:

Predict 5-year metastasis-free survival using clinical features.

Investigate the relationship between hormone receptor status (ER, PR, HER2) and prognosis.

Examine whether integrating gene expression data improves predictive performance.

Research Questions
Clinical Prediction:
How well do common clinicopathological variables predict distant metastasis within 5 years?

Hormone Receptors:
What is the relationship between survival and hormone receptor status (ER/PR/HER2)?

Genomic Integration:
Does combining clinical and gene expression data enhance predictive accuracy?

Dataset
Source: Netherlands Cancer Institute

Sample size: 295 patients

Features:

Clinical: Age, tumour size, lymph nodes, ER, PR, HER2, etc.

Genomic: 111 gene expression variables

Target: E02_EVENT_DMFS_2005 (Metastasis status after 5 years)

Methods Used
  Clinical Model
Linear Discriminant Analysis (LDA)

Variables: log-transformed Age, Tumour Size, Lymph Nodes, ER, PR

Hit Rate: 69% (without cost adjustment)

Misclassification cost used to better capture metastasis cases

  Dimensionality Reduction + KNN
Principal Component Analysis (PCA) on clinical data

K-Nearest Neighbors (KNN) using first two PCs

Hit Rate: 72.7%

  Hormone Receptor Analysis
Hierarchical Clustering (Ward's D2)

Hit Rate: 56.1%

K-Means Clustering (Elbow method for k=2)

Hit Rate: 63.5%

  Genomic Integration
PCA on 111 gene expression variables

First 34 PCs retained (80% variance)

LDA on combined clinical + genomic data

Hit Rate: 81.8% overall, but weaker for metastasis-positive group

**Key Results**
Hormone receptor positivity (ER, PR) correlates with better prognosis.

HER2-negative patients showed lower metastasis rates.

Combining clinical and genomic data increases predictive performance.

Data imbalance (71% non-metastatic) affects classification performance, particularly for LDA.
