This repository contains the data and codes used in the following work: ***Zhang, Y., Wang, F., Sui, J. (in preparation). Decoding the individual difference in self-prioritization from resting-state functional connectome.***

In this work, we attempted to use subjects’ resting-state functional connectivity to predict their individual differences in self-prioritization. The Linear SVR model based on a nested cross-validation framework was employed.

<br/>

# File Descriptions
- data
  - 3D_FC_matrix.npy – The functional connectivity matrices of all valid subjects. The order of subjects is the same as in all data files below.
  - SPE_score.npy – The SPE score (i.e., the label we predicted) of all valid subjects.
  - covariate_age.npy – The subjects’ age.
  - covariate_gender.npy – The subjects’ gender.
  - covariate_FD.npy – The subjects’ head movement (i.e., mean FD Jenkinson).
  - all_behavioural_data.xlsx - The subjects’ all behavioral data, including their scores of interdependent self and independent self.
- output
  - This folder contains files that are output during the model run, details can be seen in the code.
- codes
  - SPE_prediction.ipynb – The main notebook we used to predict and validate.
  - nested_svr_model.py – The nested SVR model we employed, which was imported into the main notebook.
  - nested_other_model.py – This file contains the function that runs different models (e.g., LASSO, ridge regression) based on the same nested-CV framework.
  - helper_functions.py – Some useful functions that were imported into the model-running functions.

<br/>

# Dependencies
The code provided in this repository was run on the following environment
- python 3.8.5
- numpy 1.19.2
- sciPy 1.7.3
- scikit-learn 0.23.2
- joblib 0.17.0

<br/>

# Updates
- v1.0 (2022-09-08): initial release.

