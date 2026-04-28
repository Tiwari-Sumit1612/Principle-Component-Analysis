# Principal Component Analysis (PCA) – Theory

## Overview

Principal Component Analysis (PCA) is a **dimensionality reduction technique** used to transform high-dimensional data into a lower-dimensional space while preserving as much information (variance) as possible.

It is widely used in:
- Data preprocessing  
- Feature extraction  
- Noise reduction  
- Visualization of high-dimensional data  

---

##  Motivation

Real-world datasets often contain:
- Redundant features  
- Correlated variables  
- High dimensionality  

These issues can:
- Increase computational cost  
- Reduce model performance  
- Make visualization difficult  

 PCA addresses these by converting data into a set of **uncorrelated variables called Principal Components**.

---

##  Key Idea

PCA finds new axes (directions) such that:

- The **first principal component (PC1)** captures the **maximum variance**
- The **second principal component (PC2)** captures the next highest variance  
- Each component is **orthogonal (independent)** to the others  

In simple terms:  
**PCA rotates the coordinate system to align with the direction of maximum data spread.**

---

##  Mathematical Steps

### 1. Standardization

Since features may have different scales, data is normalized:

X_scaled = (X - mean) / std

---

### 2. Covariance Matrix

Captures relationships between features:

Cov(X) = (1 / (n - 1)) * XᵀX

---

### 3. Eigen Decomposition

Compute:
- **Eigenvalues (λ)** → represent variance along a direction  
- **Eigenvectors (v)** → represent directions (principal components)

---

### 4. Sorting Components

Eigenvalues are sorted in descending order:

- Highest eigenvalue → most important component  
- Corresponding eigenvector → principal direction  

---

### 5. Dimensionality Reduction

Select top k eigenvectors:

W = [v₁, v₂, ..., v_k]

---

### 6. Projection

Transform data into lower-dimensional space:

Z = X · W

---

##  Explained Variance

Explained variance ratio is:

Variance Ratio = λᵢ / Σλ

 It tells how much information each principal component retains.

---

##  Application in This Project

- Original data: **3 features**  
- Reduced to: **2 principal components**  
- Dimensionality reduction: **~33%**  
- Variance retained: **~75%**  

 This demonstrates that PCA can reduce dimensionality while preserving most of the important information.

---

##  Advantages

- Reduces dimensionality  
- Removes feature correlation  
- Improves computational efficiency  
- Helps in visualization  

---

##  Limitations

- Assumes linear relationships  
- Sensitive to feature scaling  
- Reduced interpretability  

---

##  Intuition

Imagine data points forming a tilted cloud in 3D space.

 PCA finds the **best direction to view this cloud** so that:
- Maximum variance is captured  
- Dimensions can be reduced with minimal information loss  

---

##  Summary

PCA is a powerful technique that:
- Identifies the most informative directions in data  
- Reduces complexity  
- Preserves essential patterns  

It is widely used in **machine learning and data analysis pipelines**.
