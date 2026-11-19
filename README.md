# Matrix Factorization and SVD Image Compression

> Course: Programming for Descriptive and Predictive Analytics · Semester 1 · Master's in Artificial Intelligence and Data Analytics (UACJ)

## Overview

Two hands-on notebooks on classical matrix decompositions and their use in data science. The first workshop implements LU, Cholesky, QR and SVD factorizations on small dense matrices, verifying in every case that the product of the factors reconstructs the original matrix. The second applies **truncated SVD** to a 719 x 1200 grayscale image matrix and compares reconstructions at ranks 5, 20, 50 and 100 against the original.

## Repository structure

- `notebooks/matrix-factorization.ipynb` - LU, Cholesky, QR and SVD with reconstruction checks.
- `notebooks/svd-image-compression.ipynb` - rank-k image reconstruction and visual comparison.
- `data/image-matrix.csv` - 719 x 1200 grayscale matrix used as the image source.

## Methods

- `scipy.linalg.lu`, `cholesky`, `qr` and `svd` for exact decompositions.
- `numpy` for matrix arithmetic and Frobenius-style reconstruction error.
- `matplotlib` for side-by-side visualization of the compressed images.

## Results

The rank-k experiment shows the expected trade-off: rank 5 preserves only coarse structure, rank 20-50 recovers the main shapes, and rank 100 is nearly indistinguishable from the original at a small fraction of the dense representation.

## Data and requirements

The image matrix is included as a plain CSV (~21 MB). If you prefer a lighter repository, store the image as PNG/JPG and rebuild the matrix in the notebook. Python 3 with `numpy`, `scipy`, `matplotlib`, `pandas` and `jupyter` is sufficient.

## How to run

```bash
jupyter notebook notebooks/
```

Open either notebook and run all cells. No network access is required.

---
Author: Karla Maria Monroy Alvarez
