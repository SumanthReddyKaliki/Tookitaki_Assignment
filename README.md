# Tookitaki_Assignment

## Requirements
numpy==1.14.5

pandas==0.23.4

pandas-datareader==0.6.0

imbalanced-learn==0.4.3

scipy==1.2.0

## Data Exploration Insights

1) both "feature_5","feature_6" contain single value, so I removed them

2) There are many missing values in the given data. For features with continious values, fill the missing values with mean. For features with categorical features fill the missing values with mode

3) I calculated the features that were suggested by the Tookitaki Team

4) In the Ratio_currbalance_creditlimit feature there are inf and NaN values, first I replaced inf with NaN and then replaced all NaN with 0 

5) After merging new features, there are many missing values which are imputed.

6)Define continious and categorical features (which are encoded using Label Encoder)

## Creating Processed Dataset

Open `Tookitaki_Data_Preparation-Final.ipynb`. To create processed train dataset, first set `training_data = True` and the run the notebook. To create processed test dataset, first set `training_data = False` and the run the notebook.

## Model Training

Open `Tookitaki_Model_Training-Final.ipynb` and then run the notebook. I used BalancedRandomForestClassifier and then to deal with data imbalance I gave weightage to the minority class by setting `class_weight="balanced_subsample"` I got a Gini-index (gini_index = (2*AUC) - 1) of 0.3313. I got the feature importance using inbuilt BalancedRandomForestClassifier.feature_importances_ method. 

(0.0969, 'feature_7')

(0.0674, 'mean_cash_limit')

(0.0674, 'feature_52')

(0.0629, 'total_credit_limit')

(0.0518, 'average_diff_lastpaymt_opened_dt')

(0.0461, 'feature_3')

(0.0435, 'payment_history_variable_length')

(0.0397, 'Enquiries365')

(0.0362, '#Enquiries90')

(0.0315, 'mean_credit_limit')

(0.031, 'total_diff_lastpaymt_opened_dt')

(0.03, 'mean_diff_open_enquiry_dt')

(0.0289, 'mean_cur_bal_amt')

(0.0282, 'ratio_currbalance_creditlimit')

(0.0269, 'perc_unsecured_others')

(0.0233, 'feature_29')

(0.0232, 'feature_50')

(0.0216, 'feature_66')

(0.0191, 'feature_35')

(0.0184, 'total_cur_bal_amt')

(0.0183, 'payment_history_avg_dpd_0_29_bucket')

(0.0143, 'feature_39')

(0.0139, 'feature_12')

(0.0134, 'feature_30')

(0.0103, 'feature_41')

(0.0099, 'feature_69')

(0.0098, 'min_months_last_30_plus')

(0.0097, 'feature_43')

(0.0093, 'feature_36')

(0.0092, 'max_freq_enquiry')

(0.0068, 'feature_26')

(0.0063, 'feature_56')

(0.0062, 'feature_40')

(0.0057, 'feature_4')

(0.0056, 'feature_65')

(0.0056, 'feature_32')

(0.0053, 'feature_71')

(0.0051, 'feature_72')

(0.0051, 'feature_37')

(0.005, 'feature_38')

(0.0049, 'feature_51')

(0.004, 'feature_34')

(0.0037, 'feature_64')

(0.0037, 'feature_28')

(0.0037, 'feature_1')

(0.0036, 'feature_27')

(0.0032, 'feature_68')

(0.0016, 'feature_14')

(0.0015, 'feature_25')

(0.0012, 'feature_48')

## Feature Importance

![Feature Importance](../master/image.png)
