# Longitudinal IRSD Data

This repository provides the processed dataset for the Longitudinal Index of Relative Socio-Economic Disadvantage (LIRSD) in Australia (2006–2021). The dataset includes index scores for both the unweighted (LIRSD) and population-weighted (WLIRSD) versions, along with a secondary principal component (WLIRSD-PC2) that captures additional dimensions of disadvantage.

## Dataset Description

The CSV file contains one record per geographic area (e.g., SA2 or SA3) for each census year. Key variables include:

- **year**: The census year for which the index was produced.
- **SA2_CODE21** and **SA2_NAME21**: The official code and name of the Statistical Area Level 2 (SA2) under ASGS Edition 3 (2021).
- **SA3_CODE21** and **SA3_NAME21**: The official code and name of the Statistical Area Level 3 (SA3) under ASGS Edition 3.
- **SA4_CODE21** and **SA4_NAME21**: The official code and name of the Statistical Area Level 4 (SA4) under ASGS Edition 3.
- **GCC_NAME21**: The name of the Greater Capital City Statistical Areas under ASGS Edition 3.
- **STE_NAME21**: The name of the state or territory under ASGS Edition 3.
- **population**: The usual resident population of the area in that census year, sourced from TableBuilder.
- **IRSD**, **IRSAD**, **IEO**, **IER**: Socio-economic indices as provided by the ABS.
- **LIRSD**: The Longitudinal Index of Relative Socio-Economic Disadvantage, constructed via Principal Component Analysis (PCA) on raw census data.
- **LIRSD_PC2**: The score from the second principal component (PC2) of the LIRSD, representing orthogonal dimensions of disadvantage.
- **WLIRSD**: The population-weighted version of LIRSD, where each area’s score is adjusted based on its population size.
- **WLIRSD_PC2**: The population-weighted version of the second principal component.

## Method Overview

The LIRSD/WLIRSD dataset was produced using the following steps:

1. **Raw Data Selection:** Socio-economic variables were extracted from Australian Census data obtained via TableBuilder for the years 2006, 2011, 2016, and 2021.

2. **Geographical Unit Alignment:** The raw data were aligned to a consistent set of geographical boundaries, using the latest ASGS Edition 3 standards. This involved mapping earlier spatial units (e.g., Census Collection Districts in 2006) to the more current SA2, SA3, and SA4 units, ensuring that comparisons across years are valid.

3. **Inflation and Reference Adjustments:** Monetary variables were adjusted for inflation to maintain consistent reference values across different census years.

4. **Principal Component Analysis (PCA):** PCA was applied to the selected variables in two ways. First, an unweighted PCA yielded the primary socio-economic gradient, forming the basis of the LIRSD. Second, a population-weighted PCA was used to construct the WLIRSD, with WLIRSD-PC2 extracted as the second principal component capturing additional dimensions of disadvantage.

5. **Quality Assurance:** Data exclusion rules and imputation methods were employed to address missing values and ensure the robustness of the index.

## Citation

If you use this dataset in your research, please cite it as follows:

Mu, Li. (2025). Longitudinal IRSD Dataset for Australia (2006–2021). GitHub repository. [URL]

## License

This repository is licensed under the GPL v3.0 License.

For further details or questions, please refer to this README or contact the repository maintainer.
