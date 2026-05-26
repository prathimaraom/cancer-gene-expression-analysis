# Cancer Gene Expression Analysis

Differential gene expression analysis of breast cancer data using the public GEO dataset GSE2034.

## Overview
This project analyzes gene expression profiles from 286 breast cancer patients to identify genes significantly associated with cancer relapse. Using statistical methods and bioinformatics tools, I identified 63 differentially expressed genes between relapsed and non-relapsed patients.

## Dataset
- **Source:** NCBI GEO - [GSE2034](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE2034)
- **Samples:** 286 breast cancer patients (217 no relapse, 69 relapsed)
- **Genes:** 22,283 Affymetrix probe sets
- **Platform:** Affymetrix Human Genome U133A Array

## Key Findings
- Identified **63 significantly differentially expressed genes** between relapsed and non-relapsed patients
- Top upregulated genes in relapsed patients: **AURKA** and **BIRC5 (Survivin)** - both known oncogenes in breast cancer
- PCA shows subtle but detectable differences in gene expression between the two groups

## Visualizations
- Relapse distribution plot
- PCA plot of gene expression
- Volcano plot of differential expression
- Heatmap of top 50 significant genes

## Tools & Libraries
- Python, Jupyter Lab
- Pandas, NumPy, SciPy
- Matplotlib, Seaborn
- Biopython
- Statsmodels (Benjamini-Hochberg correction)

## How to Run
```bash
# Clone the repo
git clone https://github.com/prathimaraom/cancer-gene-expression-analysis.git
cd cancer-gene-expression-analysis

# Set up environment
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Download data
# Go to https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE2034
# Download GSE2034_series_matrix.txt and place in data/ folder

# Launch Jupyter Lab
jupyter lab
```

## Project Structure
```
cancer-gene-expression-analysis/
├── data/                          # Dataset and output plots
├── notebooks/
│   ├── 01_exploration.ipynb       # Data loading and PCA
│   ├── 02_differential_expression.ipynb  # T-tests and volcano plot
│   └── 03_heatmap.ipynb           # Heatmap of top genes
├── src/                           # Helper scripts
├── requirements.txt
└── README.md
```
## Author
Prathima Rao Madhavarapu