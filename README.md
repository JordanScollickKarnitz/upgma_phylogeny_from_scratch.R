# UPGMA Phylogenetic Tree (From Scratch, R)

This repository implements the **UPGMA (Unweighted Pair Group Method with
Arithmetic Mean)** algorithm from scratch using **Jukes–Cantor distances**
to construct a phylogenetic tree.

---

## 🧬 Features
- Pairwise Jukes–Cantor distance calculation
- UPGMA hierarchical clustering
- Manual distance matrix updates
- Tree structure tracking and visualization
- Designed for instructional use

---

## 🚀 Usage

```r
source("upgma_phylogeny_from_scratch.R")

## ⏱️ Runtime & Space Complexity

Let **n** be the number of sequences and **L** be the sequence length.

### Distance Calculation
- Computing Jukes–Cantor distance between two sequences takes **O(L)** time.
- For all pairwise comparisons, this step takes **O(n² × L)** time.

### UPGMA Clustering
- At each iteration, the algorithm searches the distance matrix to find the
  closest pair of clusters: **O(n²)**.
- The distance matrix is updated **n − 1** times.
- Overall clustering time complexity: **O(n³)**.

### Space Complexity
- The distance matrix requires **O(n²)** space.
- Tree storage and auxiliary data structures require **O(n)** space.
- Total space complexity: **O(n²)**.

### Practical Notes
- UPGMA assumes a **constant molecular clock** (ultrametric distances).
- While efficient for small datasets, UPGMA is not suitable for large-scale
  phylogenetics or datasets with unequal evolutionary rates.
