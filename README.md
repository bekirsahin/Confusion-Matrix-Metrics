# Confusion Matrix Metrics (TP / TN / FP / FN)

This is a small, single-page tool that calculates common **confusion-matrix metrics** from four inputs (**TP, TN, FP, FN**) and shows the results in a clean, readable way.

It’s meant for quick checks, reporting, and teaching—without notebooks, spreadsheets, or extra dependencies.

---

## What it is

In binary classification you end up with four basic counts:

- **TP** (True Positive): predicted positive & actually positive  
- **TN** (True Negative): predicted negative & actually negative  
- **FP** (False Positive): predicted positive but actually negative  
- **FN** (False Negative): predicted negative but actually positive  

From these four numbers you can compute metrics such as **Recall (TPR)**, **Precision (PPV)**, **Specificity (TNR)**, **F1**, **FPR/FNR**, **MCC**, **LR+/LR−**, **DOR**, and others.

This page puts the formulas, the values, and short interpretation in one place.

---

## Why I built it

In practice, metrics get discussed a lot—and calculated incorrectly just as often.

I wanted a simple page where I can:
- sanity-check metric values quickly
- compare models without opening a notebook
- explain results clearly (especially to non-ML teammates)
- avoid “accuracy looks fine” problems on imbalanced data

---

## When it’s useful

Typical scenarios:
- **model evaluation / debugging** (do my numbers match the pipeline?)
- **imbalanced datasets** (focus on Recall/Precision/FPR/FNR instead of Accuracy)
- **alerting systems** (track false alarms vs misses)
- **risk-sensitive work** (fraud, medical screening, security detection, QA)
- **teaching / demos** (TP/TN/FP/FN → metrics relationships)

---

## What it shows

- Derived totals (**P, N, PP, PN, Total**) computed from inputs
- Key metrics chart (0–1)
- ROC operating point (FPR, TPR)
- Full metric list with:
  - short name + long name
  - formula
  - computed value (6 decimals)
  - short interpretation

If a metric would require division by zero, the value is shown as **N/A**.

---

## How to use

1. Open the page (locally or via GitHub Pages)
2. Enter **TP, TN, FP, FN**
3. Read results from charts and the metric cards

---

## Notes

- “Positive” and “Negative” are just **class labels** (1/0).  
  They don’t mean “good/bad” in everyday language.
- This tool is designed for **binary** confusion matrices.

---

## GitHub Pages

1. Rename the HTML file to `index.html` (or place it as `index.html` in the root)
2. GitHub → **Settings → Pages**
3. Deploy from `main` branch, `/root`
4. Your page will be available under your GitHub Pages URL
