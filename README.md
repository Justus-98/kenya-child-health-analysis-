# County-Level Spatial, Temporal, and Cluster Analysis of Under-Five Child Health Outcomes in Kenya (2021–2023)

## Overview

This project presents a comprehensive data-driven analysis of under-five child health outcomes across Kenya’s 47 counties over a 30-month period (January 2021 – June 2023). The study integrates epidemiological indicators and intervention data to uncover spatial patterns, temporal trends, and underlying drivers of acute malnutrition.

The goal is to move beyond descriptive reporting and generate **actionable public health intelligence** for targeted intervention planning.

---

## Key Objectives

- Analyze relationships between **diarrhoeal disease, stunting, and acute malnutrition**
- Evaluate the effectiveness and targeting of **deworming interventions**
- Identify **spatial and temporal patterns** in child health outcomes
- Segment counties into **risk profiles using unsupervised machine learning**
- Translate statistical findings into **policy-relevant recommendations**

---

## Data Description

The dataset includes county-level aggregated indicators:

- Acute Malnutrition Cases  
- Diarrhoea Cases  
- Total Stunted Children  
- Total Dewormed Children  
- Time dimension: Monthly (2021–2023)  
- Spatial dimension: Kenya (47 counties)

---

## Methodology

### 1. Exploratory & Correlation Analysis
- Pearson correlation (linear relationships)
- Spearman rank correlation (robust non-parametric validation)

### 2. Inferential Modelling
- Multiple Linear Regression:
  
  \[
  \text{Acute Malnutrition} = \beta_0 + \beta_1(\text{Diarrhoea}) + \beta_2(\text{Stunting}) + \beta_3(\text{Deworming}) + \varepsilon
  \]

- Model diagnostics:
  - Residual analysis
  - Normality checks (Q–Q plots)
  - Heteroskedasticity assessment

---

### 3. Unsupervised Machine Learning
- K-Means clustering
- Elbow Method (optimal k selection)
- Silhouette Analysis (cluster validation)
- County-level risk profiling

---

### 4. Spatial & Temporal Analysis
- County-level comparative analysis
- Temporal trend decomposition
- Identification of high-burden hotspots

---

## Key Findings

### 1. Diarrhoeal Disease is the Strongest Driver of Acute Malnutrition
- Consistent positive relationship across Pearson, Spearman, and regression models
- Confirms infection–malnutrition cycle in under-five children

### 2. Deworming Follows a Campaign-Based Pattern
- Strong temporal “sawtooth” distribution
- Indicates reliance on Mass Drug Administration (MDA)

### 3. Structural Mismatch Between Disease Burden and Intervention Timing
- Disease burden is continuous
- Interventions are episodic

### 4. Three Distinct County Risk Profiles Identified

| Cluster | Description | Policy Implication |
|----------|------------|---------------------|
| High-Burden (≈9 counties) | Severe stunting + high diarrhoea burden | Emergency integrated WASH + nutrition interventions |
| Baseline (≈37 counties) | Moderate, stable indicators | Preventive surveillance and routine care |
| Urban Outlier (Nairobi) | High-volume, dense case reporting | Urban-tailored health delivery systems |

---

## Model Performance

- Regression R²: ~5.7%
- Overall model significance: p < 0.001
- Clustering variance explained: 75.54%

Despite low R² (common in population health data), results are statistically robust and policy-relevant.

---

## Key Visualizations

> Add images from your R Markdown output here

- Correlation heatmap  
- Elbow method plot  
- Silhouette analysis  
- K-means cluster map (Kenya counties)  
- Temporal trend plots  

---

## Tools & Technologies

- R (tidyverse ecosystem)
- ggplot2
- DT
- cluster
- broom
- leaflet (spatial visualization)
- ggcorrplot

---

## Policy Insights

- Integrate **WASH + nutrition interventions**
- Shift from purely **campaign-based deworming to hybrid delivery models**
- Use **cluster-based targeting for resource allocation**
- Prioritize **high-burden counties as integrated emergency zones**

---

## Limitations

- Linear regression on count data (future improvement: GLM / Negative Binomial)
- Limited spatial econometric modeling
- Potential underrepresentation of environmental covariates (rainfall, food prices)

---

## Future Work

- Spatial autocorrelation analysis (Moran’s I)
- Predictive modeling for outbreak detection
- Integration of climate and economic indicators
- County-level forecasting dashboard

---

## How to Run

```r
# Install dependencies
install.packages(c(
  "tidyverse", "cluster", "broom", "DT",
  "leaflet", "janitor", "ggcorrplot"
))

# Run analysis
source("scripts/main_analysis.R")
```

---

## Author

**Justus Chege Gathogo**  
BSc Statistics | Data Analysis | Public Health Analytics  
Kenya

---

## License

This project is intended for academic and portfolio use.
