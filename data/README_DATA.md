# Data Documentation — DRMI Research

## PSID-Derived Analytical Datasets

The following files are derived from PSID Public Use data. Raw PSID files are NOT included.
To reproduce from scratch, register at https://psidonline.isr.umich.edu and download:
  - Family files: 2019 Family Data (J11.xlsx), 2021 Family Data
  - Individual files: Cross-year Individual Data

| File | Rows | Cols | Description |
|------|------|------|-------------|
| DRMI_MASTER_DATASET.csv | 3,295 | 63 | Stacked 2019+2021, all analytical vars |
| drmi_study_pop_2019.csv | 2,116 | 88 | 2019 study population with DSV/DRMI |
| drmi_study_pop_2021.csv | 1,179 | 58 | 2021 study population with DSV/DRMI |
| psid_2019_with_iv.csv   | 2,116 | 91 | 2019 population merged with NDCP IV |

## Freely Available Public Datasets

| File | Rows | Cols | Source | URL |
|------|------|------|--------|-----|
| oews_wage_table.csv | 9 | 4 | BLS OEWS May 2024 | https://www.bls.gov/oes/ |
| ndcp_iv_state_year.csv | 561 | 6 | US DOL NDCP | https://www.dol.gov/wb |
| acs_state_homemaker_rates.csv | 51 | 5 | Census ACS 2022 | https://census.gov/acs |
| summary_statistics.csv | 14 | 11 | Computed (notebook output) | N/A |

## Key Variable Definitions

| Variable | Description | Source |
|----------|-------------|--------|
| IS_HOMEMAKER | 1 = wife reports 0 paid hours, >0 domestic hours | PSID |
| DEFAULT | 1 = behind on mortgage payments 60+ days | PSID |
| DSV_COMMON_W | Annualised domestic service value (winsorised), $ | PSID + BLS OEWS |
| DRMI_COMMON_W | DSV_annual / (Mortgage_Balance x 0.20), winsorised | Computed |
| CC_ANNUAL_2018 | State annual childcare cost 2018, $ (IV) | NDCP |
| LTV_W | Loan-to-value ratio, winsorised | PSID |
| DTI_PROXY_V2 | Monthly payment / monthly income | PSID |
