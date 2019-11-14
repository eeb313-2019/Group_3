# Analysis Plan

EEB313 2019 - Group Project - Hot Dawg

Alejandra Monsivais Ibarra, Jeonghoon Lee, Adeena Zahid

## Possible analyses

Create linear mixed-effects models to define the relationship between water quality and water chemistry. Must account for spatial autocorrelation.

Calculation of correlation values.

Comparison of EPT indices/Shannon evenness indices across sites (Kruskal-Wallis H test).

Need to join the two datasets by site id. Summarize the data by year and site id. Select only the relevant variables. Mutate and form a new column for EPT index per site id per year. Mutate and form a new column for Shannon evenness index per year across sites.

## Possible results tables

Table of various linear mixed-effects models and their AIC values. Summary of the best fit model.

Table of EPT indices per site per year. Table of Shannon evenness indices per year across sites.

Output of Kruskal-Wallis H test for EPT/Shannon evenness index comparisons.

## Possible results figures

Linear regression models.

Fitted vs residuals models.

Boxplots of EPT/Shannon evenness indices.

Spatial (raster) plots of EPT indices across sites. Spatial (raster) plots of Shannon evenness indices across sites.
