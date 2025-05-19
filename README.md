# Replication Package – “Low‐Carbon City Pilot Policy and Foreign Direct Investment”

## 1. Overview
This repository contains the **dataset** and **Stata 18.0 code** required to replicate all tables and figures in the paper.  
- **Dataset** `data.dta` (282 prefecture-level cities, 2005-2021)  
- **Code** `code.do` (fully commented, step-by-step)

> **Software requirement**: Stata 18.0 or newer  
> No additional user-written packages are needed.

---

## 2. File Descriptions

| File | Purpose |
|------|---------|
| `data.dta` | Main panel dataset. Each variable is labeled in-file for quick reference. |
| `code.do`  | Master do-file that executes every stage of the empirical analysis (see Section 3). |
| `README.md` | Current document. |

---

## 3. Structure of `code.do`

1. **Data Preparation**  
   - Import raw data, construct key variables, save cleaned panel.

2. **Descriptive Statistics**  
   - Produce summary tables and correlation matrices.

3. **Main Empirical Analysis**  
   - *Staggered Difference-in-Differences* to estimate the average treatment effect of the Low-Carbon City Pilot (LCCP) policy on FDI.  
   - *Spatial Diff-in-Diff* to capture spillover effects on neighboring cities.

4. **Mechanism & Heterogeneity Tests**  
   - Channels: green technological innovation, environmental governance, foreign investment structure, public behavior.  
   - Sub-samples: by resource-based city type and by region.

5. **Robustness Checks**  
   - Alternative specifications, placebo tests, and sensitivity analyses.

Running the do-file sequentially reproduces every result reported in the paper.

---

## 4. How to Reproduce

```stata
* 1. Set working directory to the folder containing this repo
cd "path/to/repo"

* 2. Open Stata 18
* 3. Run the master do-file
do code.do
