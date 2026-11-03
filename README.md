# EPA Air Quality: Hypothesis Testing

Hypothesis testing on EPA air quality data in Python, done as part of a Coursera data course. The notebook works through three decisions for an environmental think tank, using the Air Quality Index (AQI) and a 5% significance level.

## Notebook

* `epa_hypothesis_testing.ipynb`: data exploration, two-sample and one-sample t-tests, and conclusions for each hypothesis

## What it covers

* Formulating null and alternative hypotheses
* Two-sample Welch's t-test with `scipy.stats.ttest_ind(equal_var=False)`
* One-sided tests with the `alternative` argument
* One-sample t-test with `scipy.stats.ttest_1samp`
* Interpreting p-values against a 5% significance level

## Hypotheses and results

| Question | Test | Result | Decision |
|---|---|---|---|
| Is the mean AQI in Los Angeles County different from the rest of California? | Two-sample, two-sided | LA mean 16.29 vs 11.0, p about 0.0498 | Reject the null hypothesis |
| Does New York have a lower AQI than Ohio? | Two-sample, one-sided | NY mean 2.5 vs Ohio 3.33, p about 0.0304 | Reject the null hypothesis |
| Will Michigan be affected by a policy for states with a mean AQI of 10 or greater? | One-sample, one-sided | Michigan mean 8.11, p about 0.9399 | Fail to reject the null hypothesis |

## Key findings

* Los Angeles County has a statistically higher mean AQI than the rest of California, though the p-value is close to the 5% cutoff, so the result is borderline
* New York has a statistically lower mean AQI than Ohio
* There is no evidence that Michigan's mean AQI is 10 or greater, so it is not expected to be affected by the policy
* The state samples are small (9 to 14 rows each), which limits how confident the conclusions can be

## Tools

Python, pandas, numpy, scipy, Jupyter Notebook

## Data
 `c4_epa_air_quality.csv`, 
