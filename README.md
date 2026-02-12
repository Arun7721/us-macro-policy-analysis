# us-macro-policy-analysis
Empirical macroeconomic analysis of U.S. inflation, unemployment, and monetary policy using R and FRED data. This project builds a reproducible pipeline for data collection, cleaning, visualization, and regression modeling to study Phillips-curve dynamics and policy interactions from 1990 to present.
# US Macro in R: Inflation, Fed Funds Rate, and Unemployment (1990–Present)

This project is a complete R workflow to:
1) Download U.S. macro data from FRED  
2) Clean and merge into one monthly dataset  
3) Visualize trends  
4) Run baseline regressions (Phillips-curve style + policy-rate links)  
5) Export figures/tables for a report

## Project Structure
- `R/` scripts for the pipeline
- `data/raw/` cached downloads
- `data/processed/` final dataset used in models
- `output/figures/` charts
- `output/tables/` regression outputs
- `reports/report.Rmd` reproducible report

## Requirements
- R (>= 4.2 recommended)
- RStudio (recommended)
- A FRED API key (free)

## 1) Setup: Get a FRED API Key
Create a free key: https://fred.stlouisfed.org/docs/api/api_key.html

Then set it in your environment:
- Option A (recommended): create a file `.Renviron` in project root with:
  `FRED_API_KEY=your_key_here`
- Option B: set in R:
  `Sys.setenv(FRED_API_KEY="your_key_here")`

## 2) Install packages + lock versions
Open R and run:
```r
source("R/00_setup.R")
