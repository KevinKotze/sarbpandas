
<!-- README.md is generated from README.Rmd. Please edit that file -->

## SARB Quarterly Bulletin Data

*\<last updated on 2020-04-30\>*

This repository provides convenient access to the data that accompanies
the South African Reserve Bank Quarterly Bulletin for **Python** users.
Variables that are of the same frequency have been converted to `pandas`
format and have been saved using `pickle`. The names for each of these
files is as follows:

  - **sarb\_annual.pkl**
  - **sarb\_quarter.pkl**
  - **sarb\_month.pkl**
  - **sarb\_week.pkl**
  - **sarb\_day.pkl**

The column headers relate to each of the alpha-numeric codes that are
used by the SARB. The first column is reserved for the date, where the
first day of the year, quarter or month is used. In addition, the first
Monday of the week is used from weekly data. The weekly data may include
a few zeros that may have arisen on public holidays.

The most recent description file that is provided by the SARB has also
been saved in the `data` folder as `sarb_description.pkl`. An additional
`.xlsx` version of this file is included in the **desc** folder. The
layout of this file is consistent with the way in which this data is
provided.

## Installation

Download the zip folder or clone the directory to a convenient location.

## Usage

To view the data in the dataframes:

```python
>>> import pandas as pd
>>> sarb_annual = pd.read_pickle("data/sarb_annual.pkl")
>>> sarb_annual.tail()
           date  KBP1000J  KBP1005J  KBP1006J  ...  KBP7192J  KBP7192X  KBP7193J  KBP7194J
98   2015-01-01  137991.0     851.0   14021.0  ...      91.3       3.6      91.8      91.3
99   2016-01-01  149194.0       0.0   11427.0  ...      97.8       7.1      97.2      97.8
100  2017-01-01  156212.0    2410.0    9265.0  ...     102.5       4.9     103.5     102.5
101  2018-01-01  166572.0    8843.0    8890.0  ...     108.1       5.5     110.4     109.7
102  2019-01-01  165574.0   11612.0    2369.0  ...     113.1       4.6     118.1     112.7

[5 rows x 2324 columns]
```

## Historic real-time data vintages

Historic real-time data vintages, as described in the article by Dean
Croushore and Tom Stark (2001), “A Real-Time Data Set for
Macroeconomists”, *Journal of Econometrics*, vol 105, pp. 111-30, are
only currently only available in the form of **R** packages.

## Disclaimer

Please note that this is not an official release of data and I’m in no
way responsible for the results that may be produced using these data
files. Researchers are encouraged to make use of the official data
release that is available from the South African Reserve Bank.
