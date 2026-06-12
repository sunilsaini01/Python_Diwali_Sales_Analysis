<div align="center">

# 🪔 Diwali Sales Analysis

### Exploratory Data Analysis · Customer Segmentation · Retail Intelligence

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0?style=for-the-badge)](https://seaborn.pydata.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![Status](https://img.shields.io/badge/Status-Complete-2ea44f?style=for-the-badge)]()

---

*Who buys during Diwali? How much? From where? This analysis answers all three.*

</div>

---

## 📖 Table of Contents

- [Problem Statement](#-problem-statement)
- [Dataset Profile](#-dataset-profile)
- [Methodology](#-methodology)
- [Key Findings](#-key-findings)
- [Business Insights](#-business-insights)
- [Conclusion](#-conclusion)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Acknowledgements](#-acknowledgements)

---

## 🎯 Problem Statement

Diwali is India's single largest retail event — but not every customer segment behaves the same. Without understanding **who buys, what they buy, and why**, businesses are flying blind during their most critical sales window.

This project dissects Diwali transaction data across **6 behavioral dimensions** to identify high-value customer segments and high-demand product categories — enabling precise targeting, smarter inventory allocation, and higher ROI on marketing spend.

---

## 📊 Dataset Profile

<div align="center">

| Metric | Value |
|:---|:---|
| 📁 File | `Diwali_Sales_Data.csv` |
| 📋 Raw Records | 11,251 rows × 15 columns |
| ✅ Clean Records | 11,239 rows × 13 columns |
| 💰 Total Revenue | ₹10,62,49,132 (~₹10.6 Crore) |
| 🛒 Total Orders | 27,981 |
| 👥 Unique Customers | 3,752 |
| 📦 Unique Products | 2,350 |
| 📍 States Covered | 16 States · 5 Zones |
| 💼 Occupation Sectors | 15 |
| 🗂️ Product Categories | 18 |
| 🎂 Age Range | 12 – 92 years (avg 35.4) |
| 🧾 Avg Order Value | ₹9,454 |

</div>

### Column Reference

| Column | Type | Description |
|:---|:---:|:---|
| `User_ID` | int | Unique customer identifier |
| `Cust_name` | str | Customer name |
| `Product_ID` | str | Unique product SKU |
| `Gender` | str | M / F |
| `Age Group` | str | Binned age: 0-17 · 18-25 · 26-35 · 36-45 · 46-50 · 51-55 · 55+ |
| `Age` | int | Exact customer age |
| `Marital_Status` | int | 0 = Unmarried · 1 = Married |
| `State` | str | Indian state of the customer |
| `Zone` | str | North · South · East · West · Central |
| `Occupation` | str | Employment sector |
| `Product_Category` | str | Product classification |
| `Orders` | int | Number of items ordered |
| `Amount` | int | Total spend in ₹ |

> `Status` and `unnamed1` were entirely null across all 11,251 records — dropped before analysis.

---

## 🔬 Methodology

```
Raw Data (11,251 rows)
       │
       ▼
┌─────────────────────────────────┐
│        DATA CLEANING            │
│  • Drop null columns (2)        │
│  • Drop null Amount rows (12)   │
│  • Cast Amount: float → int     │
└──────────────┬──────────────────┘
               │
               ▼
┌─────────────────────────────────┐
│     EXPLORATORY DATA ANALYSIS   │
│                                 │
│  1. Gender Analysis             │
│  2. Age Group Analysis          │
│  3. State / Zone Analysis       │
│  4. Marital Status Analysis     │
│  5. Occupation Analysis         │
│  6. Product Category Analysis   │
└──────────────┬──────────────────┘
               │
               ▼
        Customer Profile
      + Business Insights
```

---

## 📈 Key Findings

### 1 · Gender

| Gender | Customers | Total Revenue | Avg Order Value |
|:---|:---:|:---:|:---:|
| Female | 7,832 | ₹7.43 Cr | ₹9,491 |
| Male | 3,407 | ₹3.19 Cr | ₹9,367 |

> Female customers account for **~70% of the customer base and ~70% of total revenue**. The gender gap is not just in volume — women also have a marginally higher average order value.

---

### 2 · Age Group

| Age Group | Total Revenue | Avg Order Value | Customer Count |
|:---|:---:|:---:|:---:|
| **26–35** ⭐ | ₹4.26 Cr | ₹9,384 | 4,541 |
| 36–45 | ₹2.21 Cr | ₹9,700 | 2,283 |
| 18–25 | ₹1.72 Cr | ₹9,175 | 1,879 |
| 46–50 | ₹0.92 Cr | ₹9,367 | 983 |
| 51–55 | ₹0.83 Cr | ₹9,954 | 830 |
| 55+ | ₹0.41 Cr | ₹9,557 | 427 |
| 0–17 | ₹0.27 Cr | ₹9,120 | 296 |

> The **26–35 cohort drives 40% of total revenue** — the clear primary acquisition target. Notably, the 51–55 segment has the **highest average order value (₹9,954)**, signaling high-spend potential in an under-targeted age group.

---

### 3 · Geography — Top 5 States by Revenue

| Rank | State | Revenue |
|:---:|:---|:---:|
| 🥇 | Uttar Pradesh | ₹1.94 Cr |
| 🥈 | Maharashtra | ₹1.44 Cr |
| 🥉 | Karnataka | ₹1.35 Cr |
| 4 | Delhi | ₹1.16 Cr |
| 5 | Madhya Pradesh | ₹0.81 Cr |

> These 5 states contribute **~60% of total revenue**. All are either Tier-1 metro hubs or high-density population centers with strong e-commerce infrastructure.

---

### 4 · Marital Status

| Segment | Revenue Share |
|:---|:---:|
| Married Women | **28.75%** of total revenue |
| Unmarried Women | ~41% |
| All Men | ~30% |

> **Married women alone drive nearly 29% of all revenue** despite being one segment among many. When combined with all female buyers, women generate **~70% of total Diwali spend**.

---

### 5 · Occupation — Top 5 Sectors by Revenue

| Rank | Sector | Revenue |
|:---:|:---|:---:|
| 1 | IT Sector | ₹1.48 Cr |
| 2 | Healthcare | ₹1.30 Cr |
| 3 | Aviation | ₹1.26 Cr |
| 4 | Banking | ₹1.08 Cr |
| 5 | Government | ₹0.85 Cr |

> IT, Healthcare, and Aviation workers are **high-income, digitally native professionals** — the ideal profile for targeted online Diwali campaigns.

---

### 6 · Product Category — Top 5 by Revenue

| Rank | Category | Revenue |
|:---:|:---|:---:|
| 1 | Food | ₹3.39 Cr |
| 2 | Clothing & Apparel | ₹1.65 Cr |
| 3 | Electronics & Gadgets | ₹1.56 Cr |
| 4 | Footwear & Shoes | ₹1.56 Cr |
| 5 | Furniture | ₹0.54 Cr |

> **Food dominates with 32% of total revenue** — likely driven by gifting culture during Diwali (sweets, dry fruits, packaged foods). Electronics and Clothing are the high-ticket lifestyle categories.

---

## 💡 Business Insights

### 🎯 Primary Target Segment
```
Married Women · Age 26–35 · UP / Maharashtra / Karnataka
Working in IT · Healthcare · Aviation
Buying: Food · Clothing · Electronics
```

### Actionable Recommendations

**1. Hyper-targeted Digital Campaigns**
Run segmented ads on Instagram, LinkedIn, and Google targeting married women aged 26–35 in UP, MH, and KA — specifically professionals in IT/Healthcare/Aviation. This segment offers maximum ROI per marketing rupee.

**2. Inventory Pre-loading**
Aggressively stock Food (gifting packs), Clothing & Apparel, Electronics & Gadgets, and Footwear **4–6 weeks before Diwali** — these 4 categories alone account for ~64% of revenue.

**3. Untapped High-Value Segment**
The **51–55 age group has the highest average order value (₹9,954)** yet is the 5th smallest cohort. Consider premium product bundles and category-specific offers to capture this under-served segment.

**4. State-wise Budget Allocation**
Focus logistics and warehouse capacity in UP, Maharashtra, Karnataka, Delhi, and MP — these 5 states drive 60% of revenue.

---

## ✅ Conclusion

> **Married women aged 26–35, based in Uttar Pradesh, Maharashtra, or Karnataka, working in IT, Healthcare, or Aviation, are the single most valuable customer profile during Diwali. They predominantly purchase Food, Clothing & Apparel, and Electronics. Any Diwali sales strategy that fails to center this segment is leaving revenue on the table.**

---

## 🛠️ Tech Stack

| Tool | Version | Purpose |
|:---|:---:|:---|
| Python | 3.8+ | Core language |
| Pandas | Latest | Data manipulation & aggregation |
| NumPy | Latest | Numerical operations |
| Matplotlib | Latest | Base chart rendering |
| Seaborn | Latest | Statistical visualizations |
| Jupyter Notebook | Latest | Interactive analysis environment |

---

## 📁 Project Structure

```
Diwali-Sales-Analysis/
│
├── 📄 Diwali_Sales_Data.csv           ← Raw transaction dataset
├── 📓 Diwali_Sales_Analysis.ipynb     ← Full EDA notebook
└── 📋 README.md                       ← Project documentation
```

---

## 🙏 Acknowledgements

- Dataset and original project by **Rishabh Mishra**
- YouTube walkthrough: [@RishabhMishraOfficial](https://www.youtube.com/@RishabhMishraOfficial)
- GitHub reference: [Python_Diwali_Sales_Analysis](https://github.com/rishabhnmishra/Python_Diwali_Sales_Analysis)

---

<div align="center">

*If this project helped you, consider giving it a ⭐ on GitHub.*

</div>
