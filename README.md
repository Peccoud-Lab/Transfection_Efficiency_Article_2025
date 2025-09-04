# Bigger Is Better Than Many: Optimizing Multi-Gene Co-Expression with Single-Plasmid Designs

> Code and data accompanying the manuscript: **“Bigger Is Better Than Many: A Strategy to Optimize Multi-Gene Co-Expression.”**  
> Connor King, Casey-Tyler Berezin, Sarah I. Hernandez, Miranda Nowak, Jean Peccoud (Colorado State University). :contentReference[oaicite:0]{index=0}

---

## TL;DR

- We combine stochastic modeling (Finite State Projection) with flow cytometry to compare **1-, 2-, and 3-plasmid** delivery of **GFP/BFP/RFP**.  
- Across **~5–16.4 kb** plasmids, entry rates are **size-independent**; the main limiter is **co-delivery of multiple plasmids to the same cell**.  
- **Single-plasmid** designs yield **higher co-transfection probability** and **tighter co-expression correlation** than multi-plasmid systems. :contentReference[oaicite:1]{index=1}

---

## Key Findings

- **Plasmid size vs. transfection efficiency:** No significant dependence from **4,966 to 16,441 bp** (linear regression slope ~5.24×10⁻¹² ± 1.56×10⁻¹¹; p=0.365). A universal entry rate constant was estimated at **2.22×10⁻⁷ ± 2.48×10⁻⁹ 1/h**. :contentReference[oaicite:2]{index=2}  
- **Vesicle co-delivery matters:** Pre-mixing plasmids modestly improves double-positive frequencies for **2-plasmid** conditions but **not** for **3-plasmid** conditions—consistent with ~**3 plasmids per lipoplex** on average. Likelihood analyses favor a **co-delivery model**. :contentReference[oaicite:3]{index=3}  
- **Single-plasmid wins:** Encoding all genes on one plasmid increases both **co-expression probability** (e.g., triple positives) and **expression-level concordance** (higher R²) compared to pre-mixed or post-mixed multi-plasmid systems. :contentReference[oaicite:4]{index=4}

---

## Repository Structure (List)

- `notebooks/Notebook1_fit_universal_rate.ipynb` — Fit universal entry rate (MCMC). :contentReference[oaicite:5]{index=5}  
- `notebooks/Notebook2_compare_models.ipynb` — Independent vs. co-delivery models. :contentReference[oaicite:6]{index=6}  
- `notebooks/Notebook3_single_vs_multi_plasmid.ipynb` — Simulations for 1/2/3-plasmid systems. :contentReference[oaicite:7]{index=7}  
- `analysis/Markdown1_linear_regression.Rmd` — Size vs. entry rate (R: emmeans/performance). :contentReference[oaicite:8]{index=8}  
- `analysis/Markdown2_stats_tests.md` — Mann–Whitney U tests (Python: SciPy). :contentReference[oaicite:9]{index=9}  
- `src/fsp_model.py` — FSP + CME operators and simulators. :contentReference[oaicite:10]{index=10}  
- `src/inference.py` — Likelihood + Metropolis–Hastings MCMC. :contentReference[oaicite:11]{index=11}  
- `data/` — Place Figshare data here (or set `DATA_DIR`). :contentReference[oaicite:12]{index=12}  
- `figures/` — Reproduced figures. :contentReference[oaicite:13]{index=13}

---

## Installation

### 1) Python
```bash
python -m venv .venv
source .venv/bin/activate  # (Windows: .venv\Scripts\activate)
pip install -U pip
pip install numpy scipy pandas matplotlib jupyter
