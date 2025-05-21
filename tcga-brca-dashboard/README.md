TCGA-BRCA Transcriptomics Expression Analysis

This project analyzes gene expression patterns in breast cancer subtypes using data from the TCGA-BRCA cohort (PanCancer Atlas). It identifies differentially expressed genes (DEGs), performs pathway enrichment, and visualizes subtype distinctions using PCA and volcano plots.

Getting Started
These instructions will help you get a local copy of the project up and running for development, exploration, or portfolio showcasing.

See Deployment if you want to run this on a live notebook platform or build it into an interactive web app.

Prerequisites
You'll need:

Python 3.8+

Jupyter Notebook or JupyterLab

pip or conda for dependency management

Basic knowledge of Pandas, Seaborn, and gene expression data

Required Python packages:
bash
Copy
Edit
pip install pandas numpy seaborn matplotlib scikit-learn gseapy statsmodels

Installing
Step 1 — Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/tcga-brca-expression-analysis.git
cd tcga-brca-expression-analysis
Step 2 — Prepare the Data
Place the following files in the /data/ directory:

brca_tcga_pan_can_atlas_2018_clinical_data.tsv (included)

data_mrna_seq_v2_rsem.txt (download manually from cBioPortal)

See data/README.md for download links and instructions.

Step 3 — Launch the Notebook
bash
Copy
Edit
jupyter notebook notebook.ipynb
Step 4 — Run a Subtype Comparison
In the notebook, choose two breast cancer subtypes to compare. The code will:

Generate a volcano plot

Identify top DEGs

Perform KEGG and GO enrichment

Save results under /results/

Running the Tests
This is a notebook-based project. All outputs are visually validated and manually reviewed. You can reproduce:

End-to-End Analysis
Choose subtype A vs B

Check PCA separation

Confirm volcano plot and enrichment results are meaningful

Functional Unit Checks
PCA separates known subtypes

Wilcoxon and FDR identify expected DEGs

Enrichr pathways align with known cancer biology (e.g., p53, cell cycle)

Deployment
You can convert this notebook into a Streamlit app for interactive use (dropdowns, plots, enrichment on demand).

To deploy as a web app:

Convert the notebook to .py script

Wrap inputs/outputs with Streamlit or Voila

Host using Streamlit Cloud, Heroku, or Binder

Built With
Pandas – data handling

Seaborn, Matplotlib – plotting

GSEAPY – gene set enrichment (Enrichr client)

Scikit-learn – PCA and preprocessing

Statsmodels – FDR correction

Contributing
Want to extend this with survival analysis, more subtypes, or ML models? Feel free to fork and submit a PR.

Please read CONTRIBUTING.md for guidelines.

Versioning
This project uses Semantic Versioning for releases.

See GitHub tags for available versions.

Authors
Jigyasa Saini – Full pipeline design, notebook implementation