# AD-TreeSHAP

Two foders are included in this repository:
- new_data_preprocess_20: contains the code for data preprocessing and the preprocessed data for the 20 features.
- new_data_preprocess_22: contains the code for data preprocessing and the preprocessed data for the 22 features.

The code is exactly simmilar for both folders, the only difference is the number of features.

## Replicating the results

### 1. Create a data folder inside with TADPOLE dataset
- Download the TADPOLE dataset from the [ADNI website](http://adni.loni.usc.edu/).
- Create a folder named `data` inside the folder `new_data_preprocess_20` or `new_data_preprocess_22`.
- Copy the TADPOLE dataset inside the `data` folder.
- Both dictionaries and csv files are needed.

### 2. Preprocess the data
- Run the `feature_extractor.py` file with the dictionary and csv files as arguments.
- The output will be a npz file with the preprocessed data.

### 3. Run the model
- Follow the `model.ipynb` to run xgboost model.
- It will save the model in pkl format

### 4. SHAP analysis
- Follow  `shap_analysis.ipynb` to run the SHAP analysis.

### 5. Individual SHAP analysis
- Follow  `ad_analysis.ipynb` or `mci_analysis.ipynb` or `cn_analysis.ipynb` to run the individual SHAP analysis.


## Some Results
**Images are generated manually**
![ad](new_data_preprocess_22\images\graph_ad.png)
*Fig: Most frequents features for Alzheimer's Disease class*

![cn](new_data_preprocess_22\images\graph_cn.png)
*Fig: Most frequents features for Cognitive-Normal class*

![mci](new_data_preprocess_22\images\graph_mci.png)
*Fig: Most frequents features for Mild Cognitive Impairment class*
