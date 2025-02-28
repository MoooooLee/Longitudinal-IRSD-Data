# Longitudinal IRSD Data

This repository provides the processed dataset for the Longitudinal Index of Relative Socio-Economic Disadvantage (LIRSD) in Australia (2006–2021). The data include index scores for both the unweighted (LIRSD) and population-weighted (WLIRSD) versions, along with a secondary principal component (WLIRSD-PC2) that captures additional dimensions of disadvantage.

## Dataset Description

The CSV file in this repository contains one record per geographic area (e.g., SA2 or SA3) for each census year. Key fields include area identifiers, the census year, and computed index scores. Below are the definitions for the variables provided:

- **year**: The census year for producing the index
- **SA2_CODE21**, **SA2_NAME21**: The official name and the corresponding code of the Statistical Area Level 2 (SA2) under Australian Statistical Geography Standard (ASGS) Edition 3 (published in 2021)
- **SA3_CODE21**, **SA3_NAME21**: The official name and the corresponding code of the Statistical Area Level 3 (SA3) under ASGS Edition 3
- **SA4_CODE21**, **SA4_NAME21**: The official name and the corresponding code of the Statistical Area Level 4 (SA4) under ASGS Edition 3
- **GCC_NAME21**: The name of the Greater Capital City Statistical Areas (GCCSA) under ASGS Edition 3
- **STE_NAME21**: the name of States and Territories in Australia under ASGS Edition 3
- **population**: The usual resident population at the areal in that census year, sourced from TableBuilder
- **IRSD**: Index of Relative Socio-Economic Disadvantage, sourced from ABS
- **IRSAD**: Index of Relative Socio-economic Advantage and Disadvantage, sourced from ABS
- **IEO**: Index of Education and Occupation, sourced from ABS
- **IER**: Index of Economic Resources, sourced from ABS
- **LIRSD**: Longitudinal Index of Relative Socio-Economic Disadvantage, constructed by PCA from raw data across all four census year
- **LIRSD_PC2**: The score derived from second principal component (PC2) during the construction of LIRSD, orthogonal dimensions of disadvantage
- **WLIRSD:** The population-weighted version of LIRSD, where each area’s score is adjusted based on its population size.
- **WLIRSD_PC2:** The score derived from second principal component (PC2) during the construction of WLIRSD, orthogonal dimensions of disadvantage

## Method Overview

The LIRSD/WLIRSD dataset was produced by aligning Australian Census data across four census cycles (2006, 2011, 2016, and 2021). Key steps include:

1. **Variable Selection and Harmonization:** A consistent set of socio-economic variables was selected. Adjustments were made for inflation in monetary variables and for changes in geographic boundaries using ABS correspondence files.
2. **Principal Component Analysis (PCA):** Both unweighted and population-weighted PCA were applied to extract the primary index (LIRSD or WLIRSD) and a secondary component (WLIRSD-PC2).
3. **Quality Assurance:** Data exclusion rules and imputation methods were employed to handle missing data and ensure robust index construction.

## Citation
If you use this dataset in your research, please cite it as follows:

Mu, Li. (2025). Longitudinal IRSD Dataset for Australia (2006–2021). GitHub repository. URL

## License
This repository is licensed under the MIT License.

For further details or questions, please refer to this README or contact the repository maintainer.
