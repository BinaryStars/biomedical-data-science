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

---

## 🧠 Why Data Scientists Should Care About Gene Expression

Every human cell contains the same DNA, but only a subset of genes is turned on in each cell — this is **gene expression**. Measuring gene expression lets us see which genes are active under certain conditions or in certain cell types.

Gene expression data is naturally represented as **vectors and matrices** — making it a perfect candidate for applying data science and machine learning techniques.

---

## 🔢 Vectors: Your First Step Into Omics

Let’s say we measure the expression of **GeneA** across five cells. We get a vector:

```python
geneA = np.array([2.1, 3.5, 1.8, 4.0, 2.9])
```

Each number represents the gene's activity in one cell. We do the same for **GeneB**:

```python
geneB = np.array([1.2, 3.3, 2.4, 3.8, 3.0])
```

Now we can begin exploring relationships between these genes.

---

## ➕ Why Add Vectors?

Adding vectors lets us look at **combined activity** — useful for genes that work together in a pathway or biological process.

```python
geneA + geneB
```

---

## 🎯 Dot Product vs. Cosine Similarity

When comparing genes, two key operations are:

### Dot Product
Measures **magnitude and alignment** — higher when genes are **strongly and similarly** expressed.

```python
np.dot(geneA, geneB)
```

### Cosine Similarity
Measures **pattern similarity**, ignoring scale — higher when genes behave similarly across cells.

```python
cos_sim = np.dot(geneA, geneB) / (np.linalg.norm(geneA) * np.linalg.norm(geneB))
```

| Metric              | Measures               | Scale Sensitive? | Use Case                         |
|---------------------|------------------------|------------------|----------------------------------|
| Dot Product         | Magnitude + Pattern    | ✅ Yes           | Strong co-expression             |
| Cosine Similarity   | Pattern Only           | ❌ No            | Trend similarity                 |

---

## 🧪 Try This Yourself

- Add a third gene vector and compare it
- Plot multiple expression patterns
- Calculate pairwise cosine similarities

---

## 📘 What's Next?

This is **Module 1** of my hands-on journey into omics. Coming next:

> Module 2: Matrices & Datasets — where gene expression matrices reveal hidden biological structure using PCA and clustering.

Follow along in the GitHub repo: [biomedical-data-science](https://github.com/BinaryStars/biomedical-data-science)

