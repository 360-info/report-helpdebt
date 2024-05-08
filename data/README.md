# `/data`

## Processed HELP loan statistics: `stats-*.csv`

Percentages of all sampled HELP debtors or all sampled taxpayers who fall into categories:

- `No debt`: no HELP debt (not included in the `alldebtors` files)
- `No repayment`: did not have a mandatory repayment due to their taxable income being too low (their balance may have increased as a result of indexation)
- `Debt reduced`: made a mandatory repayment that resulted in their balance falling by at least AU$200
- `Indexation and repayment balanced`: made a mandatory repayment, but the balance changed by less than AU$200 in either direction due to indexation
- `Debt grew despite payment`: made a mandatory repayment, but their balance grew by at least AU$200 in spite of the payment due to indexation

These files are based on 2% samples of Australian taxpayers, so these proportions are estimates. 95% confidence intervals are included with the estimated proportions. The category `Debt grew despite payment` does not appear in some years, as there are no sampled HELP debtors who fall into this category in those years.

The sample files run to 2020-21. Stats for more recent years use the 2020-21 sample file. In the files marked `-scaled.csv`, incomes have been scaled using the 2022 and 2023 Wage Price Index to investigate the sensitivity of results to changing incomes.

The 2024 statistics use these figures, plus the Wage Price Index to Dec 2023 to scale incomes. This figure is not final and is likely to change when the next estimate is released on May 15.

## Processed repayment rates: `repayment-rates.csv`

A tidied collection of the repayment rates in `/data/raw`, collected from the Australian Parliament House and Australian Taxation Office. Columns include:

- `year_end`: the end of the financial year that the rate applies to
- `repay_rate`: the repayment rate for HELP loans
- `repay_threshold`: the _upper_ threshold for which this rate applies. HELP loan repayments are not progressive; the rate applies to the entire balance if the debtor's income is below the threshold but above others. For the top rate each year, the threshold is `Inf`.

## `raw/repayment-rates-*.csv`

Raw repayment rate tables copied directly from the [APH](https://www.aph.gov.au/About_Parliament/Parliamentary_Departments/Parliamentary_Library/pubs/rp/rp2021/Chronologies/HigherEducation#_Toc67381554) and [ATO](https://www.ato.gov.au/tax-rates-and-codes/study-and-training-support-loans-rates-and-repayment-thresholds) websites. These are tidied into `repayment-rates.csv`.

## Individual tax return data

> ![warning]
> This data is not included in the repository to protect the privacy of individuals. The data is available from the Australian Taxation Office, and can be requested by [contacting them](https://www.ato.gov.au/about-ato/research-and-statistics/in-detail/taxation-statistics/taxation-statistics-previous-editions/taxation-statistics-2017-18/statistics/individuals/individuals-sample-files) and signing a confidentiality deed.

If you acquire this data, the analysis script looks for `.csv` or `.txt` files inside `/data/raw` matching the pattern `20??_sample_file`.
