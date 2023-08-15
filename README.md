# Suicide Risk Prediction
### Making the dataset
Note: Because the the output files will be saved as csv files, you will only need to do the following steps once.
1. Run make_predictors.rmd and make_response.rmd first. These pull from the mental-health folder of the ABCD v5 release and will produce two csv files called 'predictors.csv' and 'suicide_risk.csv' respectively.
2. Next run make_full_data.rmd which will combine 'predictors.csv' and 'suicide_risk.csv' to produce 'final_data_all_subj.csv', which will be used in running the models.

### Running the models
The file risk_model.rmd is meant to be a tutorial in running some of the more common classification models and assessing their performance. Some of the steps are very computationally heavy, like the training data imputation, fitting the models, and performing the Boruta variable selection. Change `eval=FALSE` to `eval=TRUE` so that you can run those code chunks. The good thing is you will only have to run these steps once because it will save the outputs as .RDS files which are basically R objects. After you run the computationally heavy code chunks once, change `eval` back to FALSE.
