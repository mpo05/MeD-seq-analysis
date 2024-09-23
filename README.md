# Analysis of the methylation profile of Myelodysplastic Syndrome patients pre and port HMA treatment

## Overview

This project analyzes DNA methylation patterns in Myelodysplastic Syndrome (MDS) patients treated with hypomethylating agents (HMAs), specifically Azacitidine (AZA) and Decitabine (DAC). The analysis focuses on identifying differentially methylated regions (DMRs) and comparing methylation patterns between responders and non-responders to HMA therapy.

## Data Processing and Analysis Steps

1. **Data Preprocessing**
   - Import and clean DMR files
   - Transform and standardize data format
   - Apply filters (e.g., FoldChange ≥ 2, ≥ 20 LpnPI-sites)
   - Split data into upwards and downwards methylated regions

2. **CpG Islands and TSS Analysis**
   - Process CpG island and Transcription Start Site (TSS) files
   - Combine data for each patient
   - Apply statistical filters (q-value ≤ 0.05)

3. **Categorization and Grouping**
   - Group data into categories: AZA Non-responders, AZA Responders, DAC Non-responders

4. **Statistical Analysis**
   - Calculate weighted mean methylation ratios
   - Perform Mann-Whitney U tests to identify significantly different methylation patterns

5. **Visualization**
   - Generate histograms of methylation ratios
   - Create bar plots of weighted mean methylation by chromosome
   - Produce violin plots showing methylation distribution across chromosomes
   - Plot boxplots of significant bins from Mann-Whitney U tests

6. **Genomic Binning**
   - Split chromosomes into 100kb bins
   - Assign methylation data to corresponding genomic bins

7. **Circos Plot Generation**
   - Generates a Circos Plot that shows the whole methylome of responders and non responders

## Scripts and Outputs

### Main Script
- `methylation_analysis.ipynb`: Contains all data processing and analysis functions

### Key Outputs
- Weighted mean methylation by chromosome
- Violin plots showing methylation distribution across patient groups
- Significant genomic bins (100kb) with differential methylation between responders and non-responders

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/mpo05/MeD-seq-analysis/.git
   ```
2. Install the required dependencies.
3. Open the notebook using Jupyter:
   ```bash
   jupyter notebook methylation_analysis.ipynb
   ```
4. Run the cells in the notebook to reproduce the analysis.

## License

This project is licensed under the MIT License.
