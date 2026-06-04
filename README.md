# Income & Overdose Deaths in Phoenix

## Overview
Observational study analyzing the relationship between median household 
income and fatal overdose rates across 42 Phoenix zip codes. Merges 
public health and census data to identify socioeconomic patterns in 
overdose deaths and inform public health policy.

## Data Sources
- Phoenix Open Data — fatal overdose counts by zip code 
  (Phoenix Fire Department & Maricopa County Medical Examiner)
- Point2Homes / U.S. Census Bureau — median household income, 
  population, and number of households by zip code (2022 ACS)
- Data not included in repo; publicly available at sources above

## Methods
- Data merging and cleaning in Python/pandas (42 zip codes)
- Descriptive statistics and correlation matrix
- OLS regression (statsmodels) with diagnostic testing
- 95% confidence intervals for regression coefficients
- Independent samples t-test (high vs. low income zip codes)
- Statistical power analysis and sample size calculation

## Key Findings
| Metric | Value |
|---|---|
| Correlation (income vs. overdoses) | -0.678 |
| R-squared | 0.460 |
| F-statistic p-value | 7.90e-07 |
| T-test p-value | 0.000018 |
| Study power (42 zip codes) | ~62% |

- Strong negative correlation: as median income increases, 
  fatal overdoses decrease
- Every $1 increase in median income associated with 0.000266–0.000548 
  fewer overdose deaths per zip code
- Model statistically significant; income alone explains 46% of variance
- 64 zip codes needed for 80% power; study slightly underpowered 
  but findings remain significant

## Implications
Findings support targeting overdose prevention resources toward 
lower-income zip codes in Phoenix. Study provides a replicable 
framework for other cities.

## Tools & Libraries
Python, pandas, statsmodels, seaborn, matplotlib, scipy, Google Colab
