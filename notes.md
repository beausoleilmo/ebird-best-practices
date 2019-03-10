- How do models deal with Date covariates? Do they just convert to a number? Why not use year as a covariate?
- Consider demonstrating using elevation and other landscape metrics via `landscapemetrics` package
- Shouldn't validation be done on calibrated predictions
- Partial dependence is uncalibrated
- 2.5 vs. 3 km prediction surface
- sampling plot, density instead of points
- change experience observer to expert
- why no year covariate in occupancy
- need to add day_of_month to occupancy
- subsampling, then split 80/20?

# exploration suggested the potential need for a quadratic effect of day_of_month,
# but preliminary explorations shows that a quadratic (i.e., `I(day_of_month^2)`) 
# was not needed: the top models produced using dredge to examine all possible
# combinations of predictor variables rarely contained this quadratic term, and
# its effect was unstable as its regression coefficient differed substantially
# between the global model and the model-averaged value.
# specify detection model