# Assisted Housing Inventory - Alachua County Analysis

A data analysis project by the ASA UF Statistics Club (listed at [stat.ufl.edu/academics/clubs](https://stat.ufl.edu/academics/clubs/)). We analyze the [Florida Assisted Housing Inventory (AHI)](http://flhousingdata.shimberg.ufl.edu/assisted-housing-inventory/results?nid=100) for Alachua County, FL. The AHI tracks government-assisted rental properties - developments that receive grants, loans, or subsidies either to the owner or directly to tenants.

**Project Director:** Yimo Liu

## Project Scope

The project runs in two stages:

**Stage 1 - Data Cleaning and Exploratory Analysis** (March 2026 - presented April 22, 2026): Ingest and clean the raw AHI data, then explore patterns across funders, properties, assistance programs, and at-risk developments. This stage is complete.

**Stage 2 - Modeling and Predictive Statistics** (Fall 2026): Build on the EDA to develop predictive models - for example, identifying developments at risk of losing assistance or forecasting changes in the assisted housing stock.

## Key Findings (Stage 1)

- **FHFC is the dominant funder**, covering more developments and assisted units than all other programs combined.
- **All 5 programs achieve at least 86% assistance rates** across their portfolios.
- **The unassisted unit gap is concentrated in just 2-3 developments**, not spread evenly across the county.
- **Assisted housing primarily serves families**, with the 55-60% AMI income tier receiving the most support - programs are not fully reaching the very lowest income households.
- **Rents are generally held below Fair Market Rent**, though with notable variation across developments.

## Repository Structure

```
Data/
  Raw Data/         Raw AHI export (Excel)
  Cleaned Data/     One CSV per dataset, produced by 01_data_cleaning.ipynb
  ahi_data_dictionary.md

Notebooks/
  01_data_cleaning.ipynb          Start here - parse raw export into analysis-ready CSVs
  02_eda_funder.ipynb             Funder-level aggregates (properties, units, assistance rates)
  03_eda_inventory.ipynb          Property-level detail (funding coverage, who is served, rents)
  04_eda_assistance_program.ipynb Assistance program breakdown
  05_eda_lost_property.ipynb      Properties that have lost or are at risk of losing assistance
  06_eda_housing_agencies.ipynb   Housing agency analysis

Outputs/
  df_funder/        Charts from notebook 02
  df_inventory/     Charts from notebook 03
  (one subfolder per dataset)
```

## Data Source

Downloaded from the Shimberg Center for Housing Studies at the University of Florida:
http://flhousingdata.shimberg.ufl.edu/assisted-housing-inventory/results?nid=100

Column definitions: http://flhousingdata.shimberg.ufl.edu/AHI-user-guide#data-dictionary

## Setup

Notebooks use standard scientific Python libraries (pandas, matplotlib). Start with `01_data_cleaning.ipynb` - it generates the cleaned CSVs that all subsequent notebooks depend on.
