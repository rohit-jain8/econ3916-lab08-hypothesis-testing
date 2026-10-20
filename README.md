# econ3916-lab08-hypothesis-testing
# Hypothesis Testing — Is Job Training Worth It?

## Objective
In this lab, I used hypothesis testing to examine whether participating in a job training program led to higher earnings and whether the results were statistically significant.

## Methodology
- Loaded the LaLonde NSW job training dataset, which included 445 individuals (185 trainees and 260 controls).
- Compared 1978 earnings between the treatment and control groups using a one-sample t-test and a two-sample Welch's t-test.
- Created a `welch_t()` function to calculate Welch's t-statistic and verified my results against SciPy for the full sample and five demographic subgroups.
- Calculated Cohen's d to measure the size of the treatment effect.
- Conducted a power analysis to evaluate the study's statistical power and estimate the sample size needed to detect an effect size of d = 0.3.
- Tested treatment effects across five overlapping demographic subgroups and applied Bonferroni and Benjamini-Hochberg corrections to account for multiple comparisons.
- Explored how p-values behave when a real effect exists versus when there is no effect, including a simulation of false-positive results.

## Key Findings
- The treatment group earned an average of \$1,794.34 more than the control group in 1978.
- The difference was statistically significant, with a Welch's t-statistic of 2.6741 and a p-value of 0.0079.
- Cohen's d was 0.2727, indicating a relatively small effect size despite the statistically significant result.
- The study's achieved statistical power was 80.8%, slightly above the 80% target.
- Before correcting for multiple comparisons, 2 of the 5 demographic subgroups showed statistically significant treatment effects. After applying the Bonferroni correction, only 1 subgroup remained significant.
- In my take-home simulation, 34 studies without a real effect and 39 studies with a real effect produced statistically significant results. This meant that 46.6% of all significant results were false positives.

Overall, this lab helped me understand the difference between statistical significance and the actual size of an effect. It also showed me why sample size, statistical power, and multiple comparisons are important when interpreting results and deciding whether a program is worth funding.
