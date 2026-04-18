# Replication of Reis et al. (2019): main reports and supporting data

[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.19642432-blue)](https://doi.org/10.5281/zenodo.19642432)

[![OSF](https://img.shields.io/badge/OSF-q7uyf-blue)](https://osf.io/q7uyf)

This repository contains the source files, input datasets, and rendered HTML reports used in the direct replication of a published preclinical systematic review and meta-analysis on the antidepressant-like effects of minocycline in rodents.

The repository currently includes two main reports:

- `meta_analyses_main_report.Rmd` / `meta_analyses_main_report.html`
- `risk_of_bias_report.Rmd` / `risk_of_bias_report.html`

## Repository contents

### Main meta-analysis files
- `meta_analyses_main_report.Rmd` – source file for the main meta-analytic report
- `meta_analyses_main_report.html` – rendered HTML version of the main meta-analytic report
- `41598_2018_36507_MOESM2_ESM.csv` – supplementary dataset from the original study used for computational reproduction
- `Complete data.csv` – reconstructed dataset used for the direct replication and RoB-adjusted analyses
- `Complete data_recycling.xlsx` – dataset used for the recycling-adjusted sensitivity analysis

### Risk-of-bias files
- `risk_of_bias_report.Rmd` – source file for the risk-of-bias comparison report
- `risk_of_bias_report.html` – rendered HTML version of the risk-of-bias report
- `Risk of bias_original.xlsx` – original review risk-of-bias dataset
- `Risk of bias_replication.xlsx` – replication risk-of-bias dataset
- `Risk of bias_original_comparison.xlsx` – paired comparison dataset from the original review
- `Risk of bias_replication_comparison.xlsx` – paired comparison dataset from the replication

### Output folders
- `report_figures/` – figures generated during rendering
- `report_tables/` – tables generated during rendering

## Requirements

The reports were written in R Markdown and require a recent R installation with the following packages:

- `rmarkdown`
- `dplyr`
- `ggplot2`
- `metafor`
- `robumeta`
- `tibble`
- `stringr`
- `gt`
- `readxl`
- `tidyr`
- `scales`
- `knitr`
- `htmltools`
- `readr`
- `forcats`
- `grid`

## Rendering the reports

To render the reports locally from R:

```r
install.packages(c(
  "rmarkdown", "dplyr", "ggplot2", "metafor", "robumeta",
  "tibble", "stringr", "gt", "readxl", "tidyr", "scales",
  "knitr", "htmltools", "readr", "forcats"
))

rmarkdown::render("meta_analyses_main_report.Rmd")
rmarkdown::render("risk_of_bias_report.Rmd")
