# TOPSIS-Charu-102303113

A Python package to implement **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** for ranking alternatives based on multiple criteria.

This project is developed as part of an academic assignment and supports:
- CSV input dataset
- User-defined weights and impacts
- Output CSV generation with **Topsis Score** and **Rank**

---

## ✅ What is TOPSIS?
TOPSIS is a Multi-Criteria Decision Making (MCDM) method used to rank alternatives by comparing their distance from:
- **Ideal Best Solution**
- **Ideal Worst Solution**

The best alternative is the one closest to the ideal best and farthest from the ideal worst.

---

## ✅ Methodology (Steps)
TOPSIS is performed using the following steps:

1. **Construct decision matrix** from input CSV  
2. **Normalize** each criteria column:
   \[
   r_{ij} = \frac{x_{ij}}{\sqrt{\sum x_{ij}^2}}
   \]
3. **Apply weights** to the normalized matrix  
4. **Determine ideal best and ideal worst** using impacts  
   - `+` means higher value is better  
   - `-` means lower value is better  
5. **Compute distance** of each alternative from ideal best and ideal worst  
6. **Calculate TOPSIS score**:
   \[
   Score = \frac{D^-}{D^+ + D^-}
   \]
7. **Rank alternatives** (Rank 1 = best)

---

## ✅ Installation (PyPI)
```bash
pip install Topsis-Charu-102303113
