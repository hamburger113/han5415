# GEOG5415M Final Assignment: Socioeconomic Deprivation and Health Outcomes in Leeds

## Project Overview
This project presents a comprehensive spatial analysis examining the relationships between socioeconomic deprivation and health outcomes across Lower Layer Super Output Areas (LSOAs) in Leeds. Utilizing the People and Places in Food Index (PPFI) alongside advanced geospatial methods, this study aims to uncover geographic inequalities and policy-relevant insights.

## Background & Context
Socioeconomic deprivation is a known determinant of poor health outcomes. This analysis focuses on the Leeds metropolitan area, integrating multidimensional deprivation data with health, education, and employment indicators.

**Key Findings:**
* **Deprivation & Health:** A strong negative association exists between deprivation and life expectancy.
* **Spatial Patterns:** Geographic clustering reveals clear segregation of health outcomes, with deprived areas concentrated in specific regions (e.g., eastern and central Leeds).
* **Mediating Factors:** Education and employment significantly mediate the relationship between deprivation and health.
* **Clustering:** Four distinct socioeconomic-health clusters were identified, suggesting the need for targeted interventions.

## Repository Contents

* **`5415Final_han.ipynb`**: The main Jupyter Notebook containing the complete code for data loading, validation, exploratory analysis, regression modeling, and visualization.
* **`data/`**: (Folder structure required) This directory should contain the source datasets used in the analysis.
* **`README.md`**: Project documentation.

## Data Description
The analysis integrates five complementary datasets. To reproduce the analysis, ensure the following files are placed in a `data/` directory relative to the notebook:

1.  **`data/ppfi_index_leeds.csv`**: **Primary Dataset (PPFI)**. A multidimensional deprivation index from the University of Leeds, combining domains like supermarket proximity, fuel poverty, and demographics.
2.  **`data/leeds_health_lsoa.csv`**: **Health Indicators**. Includes data on life expectancy, obesity rates, and mental health prevalence.
3.  **`data/leeds_education_lsoa.csv`**: **Socioeconomic Data**. Contains GCSE attainment rates.
4.  **`data/leeds_employment_lsoa.csv`**: **Socioeconomic Data**. Includes unemployment rates and employment ratios.
5.  **`data/lsoa_resident_pop_leeds.csv`**: **Population Data**. Resident population counts for normalizing data where necessary.

*Data Sources: University of Leeds, Public Health England, Data Mill North, and ONS.*

## Aims of the Code
The provided Jupyter Notebook performs the following analytical steps:

1.  **Data Validation**: Loading disparate datasets, checking for consistency, missing values, and merging them into a master spatial dataframe based on LSOA codes.
2.  **Exploratory Data Analysis (EDA)**:
    * Univariate analysis of PPFI scores, life expectancy, obesity, etc.
    * Bivariate correlation analysis to establish the deprivation-health gradient.
    * Visualization of spatial patterns and distributions.
3.  **Statistical Modeling**:
    * Multivariate regression modeling to quantify relationships.
    * Spatial clustering to identify distinct geographic zones of deprivation and health.

## Installation & Usage

### Prerequisites
* Python 3.x
* Jupyter Notebook or JupyterLab

### Dependencies
The analysis requires the following Python libraries. You can install them via pip:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn statsmodels