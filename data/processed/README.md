# Processed Data README

This folder contains the processed data used in the analysis for the study on melanoma drug resistance. These datasets are derived from raw data and have undergone preprocessing steps such as normalization and filtering for downstream analyses.

---

## **Files in This Folder**

### 1. `all.transcript_TPM.tsv`
- **Description**: This file contains transcript-level TPM (Transcripts Per Million) values for all samples in the study.
- **Format**:
  - **Rows**: Each row corresponds to a unique transcript.
  - **Columns**: 
    - The first column contains **transcript identifiers**.
    - Subsequent columns contain **TPM values** for individual samples, with column names corresponding to **sample IDs**.
- **Use**: This file is used for fine-grained expression analysis at the transcript level.

### 2. `all.gene_TPM.tsv`
- **Description**: This file contains gene-level TPM values for all samples in the study.
- **Format**:
  - **Rows**: Each row corresponds to a unique gene.
  - **Columns**:
    - The first column contains **gene identifiers**.
    - Subsequent columns contain **TPM values** for individual samples, with column names corresponding to **sample IDs**.
- **Use**: This file is used for broader expression analysis at the gene level.

---

## **Sample Renaming**

To ensure consistency in further analysis, the following sample IDs were renamed:

| Original Sample ID | Renamed as |
|---------------------|------------|
| **3B3**            | **A_1.1**  |
| **2G1**            | **A_1.2**  |
| **1E3**            | **A_4.1**  |
| **1E12**           | **A_4.2**  |
| **C10**            | **W_1.1**  |
| **C11**            | **W_1.2**  |
| **C14**            | **W_1.3**  |
| **C3**             | **W_4.1**  |
| **C4**             | **W_4.2**  |

These renamed IDs are used throughout the downstream analysis for clarity and grouping of replicates.

---

## **Data Sources**
- **Source**: These files were derived from RNA-seq data processed as follows:
  - **RNA Integrity**: Total RNA integrity was assessed using the Agilent Bioanalyzer or 4200 Tapestation. Only samples with a Bioanalyzer RIN score greater than 8.0 were used.
  - **Library Preparation**: Library preparation was performed with 5 to 10 µg of total RNA. Ribosomal RNA was removed by poly-A selection using Oligo-dT beads (mRNA Direct kit, Life Technologies). mRNA was fragmented by heating to 94°C for 8 minutes in reverse transcriptase buffer.
  - **cDNA Synthesis**: Fragmented mRNA was reverse transcribed to generate cDNA using SuperScript III RT enzyme (Life Technologies, per the manufacturer's instructions) and random hexamers. A second strand reaction was performed to create ds-cDNA. The cDNA was blunt-ended, an A base was added to the 3' ends, and Illumina sequencing adapters were ligated.
  - **Amplification and Indexing**: Ligated fragments were amplified for 12–15 cycles using primers incorporating unique dual index tags.
  - **Sequencing**: Fragments were sequenced on an Illumina NovaSeq-6000 using paired-end reads extending 150 bases.
  - **Alignment and Quantification**: RNA-seq reads were aligned and quantitated to the Ensembl release 101 primary assembly using an Illumina DRAGEN Bio-IT on-premise server running version 4.0.3-8 software.
- **Normalization**: TPM normalization was applied to account for sequencing depth and gene length.

---

## **Usage Notes**
- Ensure proper column headers are used to map samples to experimental conditions.
- Use these files in conjunction with corresponding metadata to interpret sample groupings and experimental replicates.
- These files are intended for direct use in downstream analyses such as differential expression or pathway analysis.

---

## **Contact**
For questions or additional information regarding the processed data, please contact:

- **Name**: Sophia "Noah" DeGeorgia  
- **Email**: sdegeorgia@wustl.edu  
