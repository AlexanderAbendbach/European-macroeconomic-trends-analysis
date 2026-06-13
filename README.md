# European Macroeconomic Trends Analysis

## Overview

This project analyzes European macroeconomic trends using Eurostat data accessed through a PostgreSQL database.

The analysis focuses on GDP growth, inflation, unemployment, house prices, and population across European countries. SQL is used for querying, filtering, joining, aggregation, and correlation analysis, while Python is used for exploratory analysis and visualization.

## Data

The project uses yearly country-level Eurostat indicators:

- Gdp growth: https://ec.europa.eu/eurostat/databrowser/view/tec00115/default/table?lang=en
- Inflation index: https://ec.europa.eu/eurostat/databrowser/view/prc_hicp_aind/default/table?lang=en
- Unemployment rate: https://ec.europa.eu/eurostat/databrowser/view/tipsun20/default/table?lang=en
- House price index: https://ec.europa.eu/eurostat/databrowser/view/prc_hpi_a/default/table?lang=en
- Population: https://ec.europa.eu/eurostat/databrowser/view/tps00001/default/table?lang=en

The data is accessed via a PostgreSQL database.

Broad aggregate regions such as Euro-area totals are excluded where country-level comparisons are required.

## Analysis

The notebook includes:

- Database connection and table inspection
- Data quality checks
- Common country and year selection
- GDP growth and unemployment analysis
- GDP growth and unemployment correlation
- Population growth analysis
- Negative GDP growth year analysis
- Inflation and house price index analysis
- Comparison of house price growth and consumer price growth
- Threshold analysis
- Country-level and regional visualizations

## Key Findings

- The common comparison period across all indicators is 2016–2025.
- GDP growth dropped sharply in 2020 and rebounded strongly in 2021.
- Average unemployment remained highest in parts of Southern Europe.
- GDP growth and unemployment showed a weak negative relationship.
- Consumer prices increased sharply after 2021.
- House prices grew faster than consumer prices in most countries.
- House price growth was especially strong in 2021 and 2022.
- Regional trends followed similar patterns, but with different intensity across Europe.

## Notes

This project is descriptive and exploratory. The results show macroeconomic patterns and relationships, but they should not be interpreted as causal explanations.

Some Eurostat indicators are index-based, meaning they measure changes relative to a base year rather than absolute prices.

Regional averages are simple country averages and are not population-weighted.

## Tools Used

- PostgreSQL
- SQL
- Python
- pandas
- matplotlib
- seaborn
- SQLAlchemy
  
## Repository Structure

- Data
  - Processed data
  - Raw data
- Figures
- Notebooks
- requirements.txt

## How to Run

Install the required packages:

```bash
pip install -r requirements.txt
```

Replace the password variable DB_PASSWORD with the actual password for the relevant PostgreSQL database and run the notebook:

```text
European macroeconomic trends analysis.ipynb
```

Make sure the PostgreSQL database is running before executing the SQL cells.

## Status

Complete
