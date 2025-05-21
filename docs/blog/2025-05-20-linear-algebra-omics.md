---
title: How Linear Algebra Illuminates Gene Expression Patterns
date: 2025-05-20
layout: post
---

> “If you can represent biology as vectors and matrices, you can model it, compare it, and even predict it.”

Like many people in biomedical and pharmaceutical industries, I’ve spent much of my career working with **various types of biomedical data** — from clinical to experimental — but not deeply with **omics data or its analysis**. I also hadn’t had the chance to apply **AI and machine learning techniques** to these datasets directly.

I became interested in omics because it offers a **systematic, data-rich view of biology** — the kind of foundation that’s essential for understanding complex diseases, discovering biomarkers, and enabling precision medicine. With the growing availability of open omics datasets and tools, I saw an opportunity to **learn from the ground up — hands-on**.

So I decided to learn by doing.

This blog post documents the first part of that journey: using **linear algebra** — a foundational tool in data science — to explore **gene expression data**.

🔗 View the full notebook on GitHub: [Vectors & Gene Expression](https://github.com/BinaryStars/biomedical-data-science/tree/main/notebooks/linear_algebra)
*(Please ensure `module1_vectors_gene_expression_final.ipynb` is placed in this GitHub location, or update the link accordingly.)*

---

##  Why Data Scientists Should Care About Gene Expression

Every human cell contains the same DNA, but only a subset of genes is turned on in each cell — this is **gene expression**. Measuring gene expression lets us see which genes are active under certain conditions or in certain cell types.

Gene expression data is naturally represented as **vectors and matrices** — making it a perfect candidate for applying data science and machine learning techniques.

---

##  Vectors: Your First Step Into Omics

Gene expression data can be represented using vectors. The following Python examples use the NumPy library (commonly imported as `np`) for numerical operations.

Let’s say we measure the expression of **GeneA** across five cells. We get a vector:

```python
# Ensure NumPy is imported: import numpy as np
geneA = np.array([2.1, 3.5, 1.8, 4.0, 2.9])
