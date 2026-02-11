# NCUA Data for Federally Insured Credit Unions

## About this dataset

Contains data from the National Credit Union Administration (NCUA) listing of federally insured credit unions in the United States.

- Data source: https://ncua.gov/
- Data period: Q3 2025 (September 2025)
- Disclaimer: authors not affiliated with NCUA

## Methodology

1. Download "List of Active Federally Insured Credit Unions" from https://ncua.gov/files/publications/analysis/ to [data/raw/ncua.gov/](data/raw/ncua.gov/).
    - For example, <https://ncua.gov/files/publications/analysis/federally-insured-credit-union-list-september-2025.zip>
2. Unzip it
3. Convert to CSV:
    - install prerequisites: `pip install pandas openpyxl`
    - convert XLS to CSV using pandas:
      ```python3
      import pandas as pd
      df = pd.read_excel('FederallyInsuredCreditUnions_2025q3.xlsx')
      df.to_csv('FederallyInsuredCreditUnions_2025q3.csv', index=False)
      ```
4. Extract the NCUA charter numbers to [data/processed/charter-numbers.csv](data/processed/charter-numbers.csv)

## Inventory

```
.
├── data
│   ├── processed
│   │   └── charter-numbers.csv
│   └── raw
│       └── ncua.gov
│           ├── federally-insured-credit-union-list-september-2025.zip
│           └── FederallyInsuredCreditUnions_2025q3.csv
└── LICENSE
```

## See also

- [Credit Union Website Addresses](https://github.com/credit-union-datasets/credit-union-websites) - website addresses scraped from NCUA, keyed by charter number
- [Credit Union Membership Data](https://github.com/credit-union-datasets/credit-union-membership) - membership data scraped from credit union websites
- [Credit Union HYSA Rates](https://github.com/credit-union-datasets/credit-union-hysa) - high-yield savings account rates at credit unions
