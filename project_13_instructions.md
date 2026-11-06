# Project 13: Shrinking the Cross-Section

## Overview

Given a hundred candidate return predictors, what is the stochastic discount factor? Run an unpenalized regression and you fit noise; drop everything but a handful of factors and you throw away real information. This paper shows that the right answer is economically motivated shrinkage: a prior that says the SDF should not load heavily on low-variance principal components, which turns out to be equivalent to a particular ridge-plus-lasso estimator. The resulting SDF is sparse in PC space rather than in characteristic space, and it holds up out of sample where sparse characteristic models do not.

It is one of the most directly usable pieces of research on this list. The estimator is what a multi-factor equity desk reaches for when it has more signals than history.

## Tasks

- Build the anomaly portfolio set: the 50 anomaly portfolios from CRSP and Compustat, plus the interaction-based characteristic-managed portfolios, with a summary table and a coverage figure (this is the data-cleaning deliverable)
- Replicate Table 1 (largest SDF factors, 50 anomaly portfolios) and Table 3 (largest SDF factors, models with interactions)
- Replicate the cross-validated shrinkage path: out-of-sample R² and Sharpe ratio across the two-dimensional penalty grid, which is the paper's central figure
- Replicate Table 4 (out-of-sample alpha in the withheld sample)
- Update: re-estimate on data through the present and report how the withheld-sample result looks now that the withheld sample is history

## Data sources

- CRSP and Compustat on WRDS
- Serhiy Kozak posts the MATLAB code and the supporting portfolio data at https://github.com/serhiykozak/SCS

## Notes

- The reference code is MATLAB. Porting it to a tested Python package is a legitimate and valuable part of this project—but the report has to show the ported code reproduces the original numbers, not merely that it runs.
- The same portfolio construction feeds project 14 and project 21. If two groups take those, coordinate on the build.

## Citation

Kozak, Serhiy, Stefan Nagel, and Shrihari Santosh. "Shrinking the cross-section." Journal of Financial Economics 135, no. 2 (2020): 271-292. https://doi.org/10.1016/j.jfineco.2019.06.008

## Paper PDF

[KozakNagelSantosh2020ShrinkingTheCrossSection.pdf](project_papers/KozakNagelSantosh2020ShrinkingTheCrossSection.pdf) (working paper version)
