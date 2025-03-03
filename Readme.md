# RevolutionH-tl Plot Extension

This repository provides an extension to the plots generated by RevolutionH-tl. If you encounter any issues while running the plots from RevolutionH-tl, follow the steps below to set up your environment and generate the plots successfully.

---

## Requirements

### Software and Libraries
- **Conda** (for environment management)
- **R v4.4.0** (installed via Conda)

### Additional Libraries
- `poppler`, `imagemagick`, `rust`, `ffmpeg`, `libxml2`, `librsvg`, `tesseract`

### Files
- `Module_1.R` (R script for installing required libraries)
- `RevolutionHtl_0.1.4.tar.gz` (RevolutionH-tl package)
- `tl_project.labeled_species_tree.nhx` (Newick tree file)
- `tl_project.gene_counts_reconciliation.tsv` (Gene counts file)

You can download the files from this repository.

---

## Setup Instructions

1. **Create and Activate a Conda Environment**  
   Create a Conda environment with R version 4.4.0 and activate it:
   ```bash
   conda create -n RevolutionHtl-r4.4 r-base=4.4.0 -c conda-forge
   ```
   ```bash
   conda activate RevolutionHtl-r4.4
   ```

2. **Install Required System Libraries**  
   Install the necessary system libraries using Conda:
   ```bash
   conda install -c conda-forge poppler imagemagick rust ffmpeg libxml2 librsvg tesseract
   ```

3. **Install Required R Libraries**  
   Run the Module_1.R script to install the required R libraries:
   ```bash
   Rscript Module_1.R
   ```

4. **Install the RevolutionH-tl Package**  
   Install the RevolutionH-tl package from the .tar.gz file:
   ```bash
   R CMD INSTALL RevolutionHtl_0.1.4.tar.gz
   ```

5. **Load the RevolutionH-tl Library in R**  
   Open the R environment and load the RevolutionH-tl library:
   ```bash
   R
   ```

   ```R
   library(RevolutionHtl)
   ```
6. **Generate the Plot**  
   ```R
   Plot_tree(newick_file = "tl_project.labeled_species_tree.nhx", datos_file = "tl_project.gene_counts_reconciliation.tsv", header = TRUE)
   ```

## Notes  
- `Ensure all file paths are correct when running the Plot_tree function.`
