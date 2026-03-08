# CytoBulk: Results Reproduction & Visualization Tutorials

This repository contains comprehensive **installation guides**, **result reproduction tutorials**, and **visualization notebooks** for the CytoBulk.

## Overview

CytoBulk is a method for deconvolving bulk transcriptomics data and mapping H&E histology images using single-cell reference data. This repository provides reproducible workflows and tutorials for:

- **Installation** (Conda or Docker)
- **Result Reproduction** (multiple datasets and analysis types)
- **Data Visualization** (Jupyter notebooks)

---

## 📁 Repository Structure

### 1. Installation (`install/`)

Start here to set up CytoBulk in your environment:

- **`conda_install.md`** — Installation guide for **Conda environment**
  - Clone CytoBulk repository
  - Create Conda environment from `environment.yml`
  - Install Giotto in R (required for marker detection)
  - Verify installation

- **`docker_install.md`** — Installation guide for **Docker**
  - Check Docker prerequisites
  - Pull CytoBulk Docker image
  - Verify image availability

### 2. Result Reproduction (`run_case/`)

Contains detailed tutorials for reproducing CytoBulk results on various datasets. Choose between **Conda** or **Docker** environments:

#### A. Conda Tutorials (`conda_run_case/`)
Markdown documentation for tutorials (each includes instructions to run accompanying Python scripts):

**Bulk RNA-seq deconvolution and cell mapping:**
- `bulk_deconv_*.md` — Bulk deconvolution tutorials (12_simulation, BRCA, Flu_sdy67, human_bulk, TCGA, HGSOC, etc.)

**H&E image → scRNA mapping:**
- `he_mapping.md` — General H&E mapping tutorial
- `HE_mapping_*.md` — H&E mapping tutorials for specific datasets (CID867, TCGA-37-4132, etc.)

**Spatial transcriptomics (ST) deconvolution:**
- `st_deconv_*.md` — ST deconvolution tutorials (10x_BRCA, ER2, merfish, mouse_mob, pdac, seqfishplus, TNBC, etc.)

**ST reconstruction:**
- `st_10x_mapping.md` — ST cell type mapping (maps single cells to spatial locations)

#### B. Docker Tutorials (`docker_run_case/`)
Docker-compatible documentation for running the same analyses:

**Bulk deconvolution:**
- `bulk_deconv_*.md` — Docker versions of bulk deconvolution tutorials

**H&E mapping:**
- `HE_mapping_*.md` — H&E mapping tutorials for specific datasets (CID867, TCGA-37-4132, etc.)

**ST deconvolution:**
- `st_deconv_*.md` — ST deconvolution tutorials (10x_BRCA, ER2, merfish, mouse_mob, pdac, seqfishplus, TNBC, etc.)

### 3. Visualization (`visualization/`)

Interactive Jupyter notebooks for exploring and visualizing CytoBulk results:

**Important: Required packages for visualization**

Before running Jupyter notebooks, ensure the following packages are installed in your environment:

```bash
pip install pandas numpy scanpy matplotlib seaborn scipy scikit-learn
```

Key packages:
- `scanpy` — Single-cell analysis toolkit
- `pandas` — Data manipulation
- `numpy` — Numerical computing
- `matplotlib` & `seaborn` — Data visualization
- `scipy` — Statistical tests (Mann-Whitney U, Pearson correlation, etc.)
- `scikit-learn` — Machine learning metrics (MSE, mean absolute error, etc.)

**Jupyter notebooks:**

- **`bulk_visualization.ipynb`** — Bulk RNA-seq deconvolution results
  - Visualize deconvolved cell-type fractions
  - Compare with ground truth
  - Statistical analysis and plots

- **`he_visualization.ipynb`** — H&E mapping results
  - Compare CytoBulk vs. expression-only methods
  - Gene-wise correlation and MSE metrics
  - Statistical significance testing

- **`st_visualization.ipynb`** — Spatial transcriptomics deconvolution results
  - Spatial distribution of cell types
  - Cell-type colocalization patterns
  - Comparative analysis across methods

---


