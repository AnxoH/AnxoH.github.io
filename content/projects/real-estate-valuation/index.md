---
title: Hybrid Real Estate Valuation Model
summary: A multimodal ML architecture fusing OpenAI CLIP image embeddings with XGBoost on tabular data achieves R²=0.71 for housing price prediction in Gijon, Spain.
date: 2026-06-30
type: docs
math: true
tags:
  - ML
  - Quant
  - Python
image:
  filename: featured.jpg
  focal_point: Smart
---

**Grade:** 10/10 (Proposed for Honors) · **Degree:** Mathematics (University of Oviedo)

[**📄 Download Full Thesis (PDF)**](/uploads/TFG_Matemáticas_SinNombre.pdf)

**Source Code:** [github.com/AnxoHerrera/multimodal-real-estate-valuation-model](https://github.com/AnxoHerrera/multimodal-real-estate-valuation-model)

## Overview

This thesis designs an **automated multimodal valuation system** for residential properties in Gijon, Spain. It fuses traditional tabular real estate features (size, location, rooms) with **visual quality metrics** extracted from listing photographs using OpenAI's CLIP model in zero-shot mode.

The key innovation is a **cascaded hybrid architecture (M6)** that combines an interpretable Ridge regression baseline with an XGBoost non-linear residual corrector, capturing complex threshold effects while preserving model transparency.

## Methodology

- **Data Pipeline:** Automated web scraping of property listings and interior/exterior photos, stored in a Supabase relational database
- **Visual Feature Extraction:** OpenAI CLIP zero-shot scoring across 6 dimensions using bipolar semantic prompts: luminosity, materials quality, kitchen, bathrooms, general condition, and views
- **Feature Engineering:** Non-linear spatial interactions, hedonic property ratios, and tabular-visual cross-interactions (e.g., surface $\times$ condition score)
- **Cascaded Model M6:** Ridge regression ($y^*_{\text{Ridge}}$) → XGBoost on residuals ($H(x)$) with strict regularization ($d=4$, $\eta=0.05$, $\lambda=1.0$)
- **Validation:** 10-fold cross-validation, Wilcoxon signed-rank hypothesis testing

## Key Results

- **CLIP visual features** significantly improved predictions ($p = 0.0205$), with "views" and "general condition" ranking among the top 15 most important variables
- **Cascaded hybrid model (M6):** Test $R^2 = 0.71$, MAE = 48k EUR (-14% vs linear), MAPE = 18.9% (statistically significant improvement, $p < 10^{-15}$)
- Residual error analysis revealed an empirical prediction ceiling caused by unobservable factors (judicial auctions, structural ruin, omitted photos)
