# Linear Regression from Scratch

- dataset: Boston housing
- sourced from: https://www.kaggle.com/datasets/altavish/boston-housing-dataset?resource=download

## Steps before beginning training

1. Data Imputation
   Several features in the dataset contained missing values. To handle this, we used a combination of imputation strategies depending on the nature of each feature:

   For features with low variance or skewed distributions, we used mean, median, or mode imputation, based on visual inspection of histograms and feature-target scatter plots.
   For more complex features where simple imputation wasn't appropriate, we used clustering-based imputation. Specifically:
   We applied KMeans clustering on samples with complete data (excluding the feature with missing values and the target variable) to identify natural groupings based on feature similarity.
   For each sample with a missing value, we identified its cluster and then imputed the missing value using the mean of that feature within the corresponding cluster.
