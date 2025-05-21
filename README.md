
# TCGA-BRCA Transcriptomics Expression Analysis

This project analyzes gene expression patterns in breast cancer subtypes using data from the **TCGA-BRCA cohort (PanCancer Atlas)**. It identifies **differentially expressed genes (DEGs)**, performs **pathway enrichment**, and visualizes subtype distinctions using **PCA** and **volcano plots**.

---

## Getting Started

These instructions will help you get a local copy of the project up and running for development, exploration, or portfolio showcasing.

See **Deployment** if you want to run this on a live notebook platform or build it into an interactive web app.

---

## Prerequisites

You'll need:

- Python 3.8+
- Jupyter Notebook or JupyterLab
- `pip` or `conda` for dependency management
- Basic knowledge of Pandas, Seaborn, and gene expression data

### Required Python packages:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn gseapy statsmodels
```

## Installing

### Step 1 — Clone the Repository

```bash
git clone https://github.com/your-username/TCGA-BRCA-Transcriptomics-Expression-Analysis.git
cd TCGA-BRCA-Transcriptomics-Expression-Analysis
```
### Step 2 — Prepare the Data

Place the following files in the `/data/` directory:

- `brca_tcga_pan_can_atlas_2018_clinical_data.tsv` (included)
- `data_mrna_seq_v2_rsem.txt` (download manually from [cBioPortal](https://www.cbioportal.org/))

> 📁 See `data/README.md` for download links and instructions.

### Step 3 — Launch the Notebook

Make sure you're in the project root directory, then run:

```bash
jupyter notebook notebook.ipynb
```

### Step 4 — Run a Subtype Comparison

Inside the notebook, follow these steps:

- Select two breast cancer subtypes to compare  
- The analysis will automatically:
  - Generate a volcano plot  
  - Identify top differentially expressed genes (DEGs)  
  - Perform KEGG and GO enrichment analysis  
  - Save all outputs to the `/results/` directory

## Running the Tests

This is a notebook-based project. All outputs are visually validated and manually reviewed. You can reproduce and verify results through the following checks:

### End-to-End Analysis

- Choose subtype A vs B  
- Check PCA separation  
- Confirm that the volcano plot and enrichment results are biologically meaningful

### Functional Unit Checks

- PCA effectively separates known breast cancer subtypes  
- Wilcoxon test and FDR correction correctly identify expected DEGs  
- Enrichr enrichment results align with known cancer pathways (e.g., p53 signaling, cell cycle)

## Deployment

You can convert this notebook into a **Streamlit** app for interactive use (e.g., dropdowns, plots, enrichment on demand).

### To deploy as a web app:

1. Convert the notebook to a `.py` script  
2. Wrap the necessary inputs and outputs using **Streamlit** or **Voila**  
3. Host the app using one of the following platforms:
   - [Streamlit Cloud](https://streamlit.io/cloud)
   - [Heroku](https://www.heroku.com/)
   - [Binder](https://mybinder.org/)

## Built With

- **Pandas** – for data manipulation and processing  
- **Seaborn** and **Matplotlib** – for data visualization and plotting  
- **GSEAPY** – for gene set enrichment analysis using the Enrichr API  
- **Scikit-learn** – for PCA and preprocessing tasks  
- **Statsmodels** – for statistical tests and FDR correction

## Contributors

- **Jigyasa Saini** – Full pipeline design and notebook implementation  
