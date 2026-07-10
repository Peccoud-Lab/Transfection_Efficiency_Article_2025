# Bigger Is Better Than Many: Optimizing Multi-Gene Co-Expression with Single-Plasmid Designs

> Code and data accompanying the manuscript: **“Bigger Is Better Than Many: A Strategy to Optimize Multi-Gene Co-Expression.”**  
> Sarah I. Hernandez, Casey-Tyler Berezin, Miranda Nowak, Jean Peccoud, Connor King.

---
## Repository Structure (List + Brief Descriptions)

- `Figures/` — Exported plots and panels used in the manuscript.
- `Folder1-Flow_Cytometry_Data/` — flow cytometry data and metadata used by the notebooks and markdown files
- .
- `Folder2-Model_Parameter_Fits/` — Saved model fit outputs from Notebook1.
- `Notebook1-Transfection_Model_Fitting.ipynb` — Fits the transfection model to data (MCMC) and writes results to `Folder2-Model_Parameter_Fits/`.
- `Notebook2-Transfection_Model_Predictions_Plasmid_Number.ipynb` — Uses fitted parameters to simulate pre and post-mixed systems performs Mann-Whitney U test comparing these two systems.
- `Notebook3-Transfection_Model_Predictions_Size.ipynb` — Uses fitted parameters to simulate outcomes for single plasmid system and performs Mann-Whitney U test comparing to multi-plasmid systems.
- `Markdown1-Transfection_Rate_Constant_vs_Size.Rmd` — RMarkdown analysis testing whether the transfection/entry rate depends on plasmid size; runs regression + diagnostics.
- `Markdown2-Coexpression_Level_Analysis.Rmd` — RMarkdown analysis of co-expression metrics (e.g., double/triple-positive fractions, correlation of reporters) and MFI for single vs. multi-plasmid conditions.
