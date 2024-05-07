# `/data`

## Processed data: `stats-*.csv`

Percentages of all sampled HELP debtors or all sampled taxpayers who fall into categories:

- `No debt`: no HELP debt (not included in the `alldebtors` files)
- `No repayment`: did not have a mandatory repayment due to their taxable income being too low (their balance may have increased as a result of indexation)
- `Debt reduced`: made a mandatory repayment that resulted in their balance falling by at least AU$200
- `Indexation and repayment balanced`: made a mandatory repayment, but the balance changed by less than AU$200 in either direction due to indexation
- `Debt grew despite payment`: made a mandatory repayment, but their balance grew by at least AU$200 in spite of the payment due to indexation

These files are based on 2% samples of Australian taxpayers, so these proportions are estimates. 95% confidence intervals are included with the estimated proportions. The category `Debt grew despite payment` does not appear in some years, as there are no sampled HELP debtors who fall into this category in those years.

The sample files run to 2020-21. Stats for more recent years use the 2020-21 sample file. In the files marked `-scaled.csv`, incomes have been scaled using the 2022 and 2023 Wage Price Index to investigate the sensitivity of results to changing incomes.

The 2024 statistics use these figures, plus the Wage Price Index to Dec 2023 to scale incomes. This figure is not final and is likely to change when the next estimate is released on May 