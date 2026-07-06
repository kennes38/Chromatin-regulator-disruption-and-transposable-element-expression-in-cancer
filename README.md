# Chromatin-regulator-disruption-and-transposable-element-expression-in-cancer
Analysis code for an MSc Genomic Medicine project investigating TE/ERV expression in PRC2-, histone modifier- and SWI/SNF-altered cancers using TCGA/REdiscoverTE and MPNST RNA-seq/SalmonTE data.
## Project Overview

This repository contains notebooks and scripts used to investigate whether disruption of chromatin regulators is associated with altered TE and ERV expression in cancer.

The project has two linked arms:

1. A pan-cancer TCGA analysis using REdiscoverTE TE expression estimates and matched chromatin regulator-altered versus wild-type tumour comparisons.
2. An independent malignant peripheral nerve sheath tumour (MPNST) RNA-seq analysis using SalmonTE and DESeq2 to compare PRC2-loss and PRC2-intact tumours.

Together, these analyses tested whether chromatin regulator disruption produces broad ERV derepression or more context-dependent TE expression changes.

## Main Analyses

### TCGA Chromatin Regulator Analyses

The TCGA analysis identifies loss-of-function mutations and candidate homozygous deletions affecting selected chromatin regulator genes, matches altered tumours to wild-type controls, and compares TE expression using REdiscoverTE-derived expression values.

The main gene sets were:

- Core PRC2 genes
- Histone modifier genes
- SWI/SNF chromatin-remodelling genes
- Selected individual or grouped chromatin regulator models

Key notebooks and scripts:

- `20.1_prc2_LoF_HomDel.ipynb`
- `20.2_prc2_TEdata_overlap.ipynb`
- `20.3_prc2_WT_matching_tumour_only.ipynb`
- `20.4_prc2_TE_differential_expression.ipynb`
- `01_histone_modifier_LoF_HomDel.ipynb`
- `02_histone_modifier_TEdata_overlap.ipynb`
- `03_histone_modifier_WT_matching_tumour_only.ipynb`
- `04_histone_modifier_TE_differential_expression.ipynb`
- `01_swi_snf_LoF_HomDel.ipynb`
- `02_swi_snf_TEdata_overlap.ipynb`
- `03_swi_snf_WT_matching_tumour_only.ipynb`
- `04_swi_snf_TE_differential_expression.ipynb`
- `TE_DE_purity_immune_stromal_adjusted_models.ipynb`
- `21_individual_gene_LoFHomDel_from_existing_outputs.ipynb`
- `22_individual_gene_TEdata_overlap.ipynb`
- `23_individual_gene_WT_matching_tumour_only.ipynb`
- `24_individual_gene_TE_differential_expression.ipynb`
- `GENCODE_coordinate_verification_all_15_genes.ipynb`
- `generic_chromatin_loss_workflow.R`
- `prc2_tcga_loss_workflow.R`

### MPNST RNA-seq Analysis

The MPNST analysis uses public RNA-seq data to quantify TE expression directly from FASTQ files with SalmonTE. TE count matrices were analysed with DESeq2 to compare PRC2-loss and PRC2-intact MPNSTs.

Key notebooks:

- `25.1_MPNST_data_discovery_and_manifest.ipynb`
- `25.2_MPNST_TE_count_pilot.ipynb`
- `25.3_MPNST_TE_count_full_run.ipynb`
- `25.4_MPNST_TE_differential_expression.ipynb`








