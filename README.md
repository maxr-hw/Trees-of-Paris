# 🌳 Paris Trees Dataset Cleanup & Analysis

A small Python project to clean and filter the **Paris public trees dataset**, extract only trees inside *Paris intra-muros*, and classify them into 5 broader ecological groups for analysis or game/map usage.

---

## 📊 Dataset Used

- Source: *Les arbres* dataset from [https://opendata.paris.fr/explore/dataset/les-arbres/]
---

## ✅ Features Implemented

This script:

1. Loads the raw CSV file
2. Cleans the arrondissement field to only keep the number (e.g., `"PARIS 18E ARRDT"` → `18`)
3. Filters trees inside **Paris intra-muros** (arrondissements 1 to 20)
4. Removes trees with missing or invalid height values
5. Keeps only genera with **1,000 or more recorded trees**
6. Creates a new CSV containing only:
   - `Arrondissement`
   - `Coordonnée 2D` (GPS position)
   - `Type d’arbre` (Genus)
7. Regroups tree genera into **5 broad ecological categories**
8. Exports a new cleaned CSV for usage

---

## 🌿 5 Tree Categories

| Category | Description | Example Genera |
|--------|-------------|----------------|
| **Tall / Shade Trees** | Large street trees providing shadow | Platanus, Tilia, Quercus |
| **Ornamental Trees** | Decorative trees for urban aesthetics | Acer, Magnolia, Ginkgo |
| **Fruit Trees** | Trees producing edible fruits | Malus, Pyrus, Prunus |
| **Conifers / Evergreens** | Needle or evergreen structure trees | Pinus, Taxus |
| **Resilient Urban Trees** | Robust planting (includes nitrogen-fixers etc.) | Aesculus, Robinia, Celtis |

---

## 🧠 How to Run the Script

### 🔹 Prerequisites

Make sure you have Python 3.10+ and install:

```bash
pip install pandas requests
```
