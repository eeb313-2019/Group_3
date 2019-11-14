# Analysis Plan

EEB313 2019 - Group Project - Hot Dawg

Alejandra Monsivais Ibarra, Jeonghoon Lee, Adeena Zahid

## Possible Analyses
Initially, the relationship between water chemistry and water quality (EPT) index will need to be found. The Purpose of the following sections (EPT Index Data Wrangling, Water Chemistry Data Wrangling, Creating the Final Data Set,Creating mixed effects models) will be to determine which, if any of the analyzed chemicals had a significant effect on EPT values. 

**EPT Index Data Wrangling**<BR>

<BLOCKQUOTE>1.)Taking the original data set, the select() function will be used to select the variables necessary for EPT calculation. These variables are (Abundance, Taxa, Site ID and Year).<BR>

2.)group_by()function will be used to bin the data set by site ID and by Year. <BR>
3.)mutate() function will be used to calculate and create a new column for EPT index by site ID and Year. </BLOCKQUOTE>

**Water Chemistry Data Wrangling**<BR>
<BLOCKQUOTE>1.) select() function will be used to select the variables necessary for analysis. These are (Nitrogen CONC, Phosphorus CONC, Dissolved Oxygen content, temperature, Site ID and Year. <BR>

2.) group_by() function will be used to bin the data set by Site ID and Year. <BR>

3.) The significant predictors will be categorized into low, moderate and high treatments, based on industry standards for water chemical content. These categories will then be used to group sites by predictor category so that we have three site groups: one with low water concentrations of the significant predictors, one with moderate and one with high.</BLOCKQUOTE>

**Creating the Final Data Set**<BR>

<BLOCKQUOTE>1.) left_join() function will be used to join the EPT data set with the Water Chemistry data set therefore creating the final data set. </BLOCKQUOTE>
  
**Creating mixed effects models**<BR>
<BLOCKQUOTE>1.)a mixed effects model will be created using EPT index as the Response Variable and;<BR>
<U>Fixed effects:</U> Nitrogen concentration, Phosphorus concentration, Dissolved Oxygen concentrations and their interactions<BR>
<U>Random effects:</U> nestedness of each of those factors by site and by year. <BR>
    2.) The dredge() function will be used to compare AIC values to determine model of best fit. If multiple models have similarly low AIC values, model averaging will be used to obtain model of best fit. <BR>
    3.)The summary() function will be used to obtain the slope values for each model and that will be used to decide which of the predictors is the main effect on the responce variable.<BR>
    4.)Slope values for the models will be used as an indicator of stregth and direction of the relationship between the random effect variables and the fixed effect variables. </BLOCKQUOTE>

## Possible Results Figures and Tables<BR>
After having determined which, if any of the chemichals analyzed had an effect on EPT values the results will be displayed in the following tables and graphs:
<BLOCKQUOTE>1.) A summary table with the following columns will be produced; Model, AIC values, weights. <BR>
  2.)A scatter plot with the predictors of the best fit model on the X axis (N,P,DO or an interaction between some combination of the former), and EPT index values on the Y axis will be made. Each point on the graph will represent a Site ID and Year. If multiple predictors show significant effects, we will facet wrap the plot by predictors so that a series of graphs each with a different predictor variable on the X axis will be made. <BR>
  3.)A map of the Mississippi river will be shown and coloured by two gradients - one which will depict values of the significant predictor from the best-fit model, and another that will depit EPT values for sampling sites along the river. The legend for each of these gradients will include numeric values associated with each colour.<BR>
  4.)A boxplot with three groups on the x-axis consisting of site groups low, moderate and high concentrations of the significant predictors. EPT-values will be on the y-axis to show distribution (median, variation and outliers) of EPT values across sites with differing water chemical contents.<BR>
  5.)A map of the land surrounding the 100 km of the Mississipi river north of the Gulf of Mexico. This map will show land use type around the river and will be compared to the raster plots in the discussion to see if certain land use types affect water quality in the Mississipi river. </BLOCKQUOTE>

