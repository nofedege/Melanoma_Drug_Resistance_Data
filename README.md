# RNA-Seq Analysis and Figure Generation for Transcriptional control of Sox10 enhancer elements as drivers of phenotype plasticity and drug resistance in melanoma


## Overview
This repository contains all scripts, code, and processed data necessary to reproduce the analyses and figures in our paper:  
**"Transcriptional control of Sox10 enhancer elements as drivers of phenotype plasticity and drug resistance in melanoma"** by Sophia DeGeorgia and Charles Kaufman.  

The study investigates the role of SOX10 enhancer elements in melanoma biology, particularly their impact on transcriptional regulation and phenotype plasticity in the context of melanoma drug resistance

Key analyses include:  
- **RNA-Seq differential expression analysis**
- **Gene Set Enrichment Analysis (GSEA)**
- **Principal Component Analysis (PCA)**
- **Synergy drug interaction analysis**
- **qPCR and growth curve comparisons**


## Scripts
Each script in the `scripts/` folder is modular and focuses on specific analyses or figure generation:

- **`scripts/PCA_analysis.R`**  
  Performs PCA on RNA-Seq data and generates plots for cell lines (Figure 3 in the manuscript).

- **`scripts/GSEA_analysis.R`**  
  Runs Gene Set Enrichment Analysis using fgsea, generates enrichment plots for key pathways.

- **`scripts/synergy_analysis.R`**  
  Computes synergy scores using drug interaction data and creates surface plots and heatmaps (Figure 5 in the manuscript).

- **`scripts/qPCR_growth_curve_analysis.R`**  
  Analyzes qPCR data and cell growth curves, producing bar plots and growth trends for comparison across cell lines.

- **`scripts/differential_expression.R`**  
  Identifies significantly upregulated and downregulated genes for each cell line, calculates shared genes, and creates heatmaps.

## Requirements
The scripts were written in R and require the following packages. To install them, run the provided `install_dependencies.R` script:
```r
# Install necessary R packages
install.packages(c("tidyverse", "fgsea", "ggplot2", "pheatmap", "dplyr", "Biostrings", "cluster"))
