# Power Method for Dominant Eigenvalue Computation

## Project Overview
This project implements the **Power Method**, a classical iterative algorithm used to compute the **dominant eigenvalue** (the eigenvalue with the largest magnitude) and its corresponding eigenvector of a matrix. The Power Method is widely applied in areas such as:

- **Google PageRank algorithm**  
- **Stability analysis of systems**  
- **Principal Component Analysis (PCA)**

Through this project, you'll learn about iterative methods, convergence behavior, and numerical analysis for eigenvalue problems.

---

## Objectives
- Implement the Power Method in Python.
- Test the algorithm on different sample matrices.
- Analyze **convergence speed** and **accuracy**.
- Visualize the results and document observations.

---

## Methodology
1. **Initialize** a random vector `x0`.
2. Iteratively compute:  
   \[
   x_{k+1} = \frac{A x_k}{\|A x_k\|}
   \]
3. Approximate the **dominant eigenvalue** as:  
   \[
   \lambda_k = \frac{x_k^T A x_k}{x_k^T x_k}
   \]
4. Repeat until convergence (i.e., until successive eigenvalue estimates change below a small tolerance).

---

## Implementation

**Requirements:**
- Python 3.x
- Libraries: `numpy`, `matplotlib` (for optional visualization)

**Example Usage:**
```python
import numpy as np
from power_method import power_method

# Define a sample matrix
A = np.array([[4, 1],
              [2, 3]])

# Run the Power Method
dominant_eigenvalue, dominant_eigenvector = power_method(A, tol=1e-6, max_iter=1000)

print("Dominant Eigenvalue:", dominant_eigenvalue)
print("Dominant Eigenvector:", dominant_eigenvector)
