# Chromatin Regulator Disruption and Transposable Element Expression in Cancer

Analysis code for an MSc Genomic Medicine project investigating transposable element (TE) and endogenous retrovirus (ERV) expression in cancers with disruption of PRC2, histone modifier and SWI/SNF chromatin-remodelling genes.

## Project Overview

This repository contains notebooks and scripts used to investigate whether disruption of chromatin regulators is associated with altered TE and ERV expression in cancer.

The project has two linked analysis arms:

1. A pan-cancer TCGA analysis using REdiscoverTE TE expression estimates to compare chromatin regulator-altered primary tumours with matched wild-type controls.
2. An independent malignant peripheral nerve sheath tumour (MPNST) RNA-seq analysis using SalmonTE and DESeq2 to compare PRC2-loss and PRC2-intact tumours.

Together, these analyses tested whether chromatin regulator disruption is associated with broad ERV derepression or more context-dependent TE expression changes.

## Repository Contents

This repository is intended to share analysis code only. Raw sequencing files, downloaded reference resources, large intermediate files and full generated result outputs are not included.

Suggested organisation:

```text
notebooks/
  01_tcga_prc2/
  02_tcga_histone_modifiers/
  03_tcga_swi_snf/
  04_tcga_individual_gene_models/
  05_mpnst_salmonte/

scripts/
  helper_workflows/
  figures/
  supplementary_tables/

docs/
  file_manifest.md
text'''

**## Main Analyses**

**##TCGA Chromatin Regulator Analyses**

The TCGA analysis identifies loss-of-function mutations and candidate homozygous deletions affecting selected chromatin regulator genes, matches altered tumours to wild-type controls, and compares TE expression using REdiscoverTE-derived expression values.
The main chromatin regulator groups analysed were:
core PRC2 genes;
histone modifier genes;
SWI/SNF chromatin-remodelling genes;
selected individual or grouped chromatin regulator models.
Key notebooks and scripts include:
20.1_prc2_LoF_HomDel.ipynb
20.2_prc2_TEdata_overlap.ipynb
20.3_prc2_WT_matching_tumour_only.ipynb
20.4_prc2_TE_differential_expression.ipynb

01_histone_modifier_LoF_HomDel.ipynb
02_histone_modifier_TEdata_overlap.ipynb
03_histone_modifier_WT_matching_tumour_only.ipynb
04_histone_modifier_TE_differential_expression.ipynb

01_swi_snf_LoF_HomDel.ipynb
02_swi_snf_TEdata_overlap.ipynb
03_swi_snf_WT_matching_tumour_only.ipynb
04_swi_snf_TE_differential_expression.ipynb

TE_DE_purity_immune_stromal_adjusted_models.ipynb

21_individual_gene_LoFHomDel_from_existing_outputs.ipynb
22_individual_gene_TEdata_overlap.ipynb
23_individual_gene_WT_matching_tumour_only.ipynb
24_individual_gene_TE_differential_expression.ipynb

GENCODE_coordinate_verification_all_15_genes.ipynb
generic_chromatin_loss_workflow.R
prc2_tcga_loss_workflow.R

**## MPNST RNA-seq Analysis**

The MPNST analysis uses public RNA-seq data to quantify TE expression directly from FASTQ files with SalmonTE. TE count matrices were analysed with DESeq2 to compare PRC2-loss and PRC2-intact MPNSTs.
Key notebooks include:
25.1_MPNST_data_discovery_and_manifest.ipynb
25.2_MPNST_TE_count_pilot.ipynb
25.3_MPNST_TE_count_full_run.ipynb
25.4_MPNST_TE_differential_expression.ipynb

**## Data Sources**

This project used publicly available or controlled-access datasets and external reference resources, including:
TCGA genomic and clinical data;
REdiscoverTE pan-cancer TE expression estimates;
GENCODE gene annotation;
public MPNST RNA-seq metadata and FASTQ files;
SalmonTE human repeat reference files.
These data files are not redistributed in this repository.

**## Files Not Included**

The following files are intentionally excluded because they are large, externally generated, controlled access, or reproducible from the analysis code:
raw FASTQ files;
downloaded TCGA/GDC files;
downloaded REdiscoverTE resources;
SalmonTE output directories;
large TE count matrices;
full differential expression result tables;
generated thesis figures and appendix tables;
local software installations, virtual environments and containers.

**##Software**

The analyses were performed using R, Bioconductor and Jupyter Notebook. Main tools and packages included:
limma;
DESeq2;
SalmonTE;
tidyverse packages;
TCGA data access and processing packages;
ggplot2 and related plotting packages.
Exact package versions may vary between environments. The notebooks contain the analysis code and can be adapted to local paths and software installations.

**##Reproducibility Notes**
The notebooks are numbered approximately in the order in which analyses were performed. Some paths reflect the original JupyterHub project structure and may need to be edited before rerunning the code in a new environment.
The MPNST analysis requires SalmonTE to be installed or otherwise available, together with the relevant FASTQ files. The TCGA analyses require access to the relevant TCGA data and REdiscoverTE expression resources.

**##Project Context**
This repository accompanies an MSc Genomic Medicine thesis investigating chromatin regulator disruption and TE expression in cancer. It is provided to support transparency and reproducibility of the analysis workflow.
