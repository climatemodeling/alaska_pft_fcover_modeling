# Alaskan-arctic PFT-level fractional cover map
These notebooks examplify how to map fractional cover of several tundra plant functional types (PFTs) using a harmonized plot inventory (Stecker et al., 2024, in preparation) and high-resolution satellite-derived predictors, including Sentinel-1, Sentinel-2, and ArcticDEM. 

## Step 1: feature preparation
This notebook demonstrates how features from Sentinel and ArcticDEM data were generated, and ensures that the input satellite-derived features are at same scale and format. Details can be found at `feature_preparation_demo.ipynb`

## Step 2: initial regression modeling
This notebook demonstrates how to identify the best random forest model for each PFT, which is then selected for model tuning for regional-scale mapping of fCover. Details can be found at `regression_modeling_initial.ipynb`

## Step 3: random forest model tuning and quality control to enhance the quality of plot samples
This code shows demonstrates the model tuning for each PFT using the best model settings from the initial regression model;
- Low quality plots identified by Cook's distance is selected for quality analysis, which reveals the controlling factor accounting for the low association between plot and satellite data;
- The importance of features used for regression modeling is also analyzed.
More details can be found at `model_tuning_feature_importance_qa.ipynb`

## Step 4: fCover regression model training and validation
This code provides an example for identifying high-quality samples using Cook's distance for both model validation and training. More details can be found at `validation_plot_generation.ipynb`

---
Citation:
Zhang T., Steckler M., Breen A., Hoffman F.M., Hargrove W.W., Kumar J., 2024. Estimating Fractional Cover of Arctic Tundra Plant Functional Types on the North Slope of Alaska Using Sentinel and Harmonized Plot Observations. In prep.
