# Southern Illinois summer-storm rainfall (1960–1964)

The authoritative numerical sources are the five original files
[`illinois60.txt` through `illinois64.txt`](https://github.com/opherdonchin/ProbabilisticMachineLearning/tree/main/Lectures/L02_Exponential_Families/generated/),
one for each summer (1960, 1961, 1962, 1963, 1964). They are reproduced from
John A. Rice, *Mathematical Statistics and Data Analysis*, 3rd edition
(Le Cam–Neyman Illinois summer-storm example), via the
[Western University teaching mirror](https://fisher.stats.uwo.ca/faculty/kulperger/SS3858/Data/).
[MIT 18.443 Project 2](https://live.ocw.mit.edu/ans7870/18/18.443/s15/projects/Rproject2_script2_gamma_MOMwithMLE.html)
also uses these five filenames. Its published Gamma fit differs slightly from
the course's verified numeric fit; the course does not claim byte identity
with MIT's input files.

Two derived CSV views contain the **same 227 positive observations** in exactly
the same order, with no missing-value removal, rounding, unit conversion or
reordering:

- [`illinois_rainfall_inches.csv`](illinois_rainfall_inches.csv):
  one `rainfall_inches` column; retained for compatibility with the existing
  Colab-first Gamma notebook.
- [`illinois_rainfall_by_year.csv`](illinois_rainfall_by_year.csv):
  `year,rainfall_inches` columns; the original year is restored for each row.

| Summer | Recorded rainfall amounts (event count) |
|---|---:|
| 1960 | 48 |
| 1961 | 48 |
| 1962 | 56 |
| 1963 | 37 |
| 1964 | 38 |
| **Total** | **227** |

For a Poisson model of counts **per summer**, the maximum-likelihood rate is
`227/5 = 45.4` recorded events/summer. The unbiased sample variance of these
five counts is `62.8` (dispersion ratio `62.8/45.4 ≈ 1.38`). These numbers
come from the annual files, not invented or inferred dates.

**Scientific limits:** Each row is a network-average rainfall amount for a
*recorded* summer storm, measured in inches, not a date/time-stamped or local
gauge-specific precipitation record. The source files establish annual grouping
but do not independently establish complete capture of all storms, a common
sampling effort, an objective storm inclusion threshold, event independence, or
unchanging occurrence rate. If counts depend on recording or inclusion rules,
the Poisson model describes the recorded-event process, not automatically all
meteorological storms. Five summers are insufficient to validate annual-count
equidispersion or long-term return-level extrapolation. The Gamma fit treats
positive recorded amounts as conditionally IID; the Poisson–Gamma calculation
additionally assumes counts independent of positive amounts and independent,
stationary summers.

**Verification (2026-10-26):** Source copies were checked against separately
uploaded originals; the numeric concatenation of the five committed annual
files was checked value-for-value and in order against the existing
`illinois_rainfall_inches.csv` in the student mirror. Source arrays have
48, 48, 56, 37, 38 values. Total rainfall is 50.937 inches across the
network-average events, and the sum of logarithms of numeric inch measurements
is approximately -672.8699945705858. The year-labeled CSV was built from
these verified files and the source order. Do not infer within-summer dates
or durations from file order.
