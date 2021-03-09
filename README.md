# KKBox: Predicting Customer Behavior for Music Streaming Services
## 1. Overview
 - The Project Goal is to Predict Customer Churn.
 - We will Predict whether a Customer that have expired his/her Membership for KKBox, will come back for a new Contract, or Cease his/her Membership with the Service.

## 2. Available Data
The Data can be Downloaded from
[This kaggle Competition link](https://www.kaggle.com/c/kkbox-churn-prediction-challenge/data).
### transactions.csv
transactions of users up until 2/28/2017.
 - msno: user id
 - payment_method_id: payment method
 - payment_plan_days: length of membership plan in days
 - plan_list_price: in New Taiwan Dollar (NTD)
 - actual_amount_paid: in New Taiwan Dollar (NTD)
 - is_auto_renew
 - transaction_date: format %Y%m%d
 - membership_expire_date: format %Y%m%d
 - is_cancel: whether or not the user canceled the membership in this transaction.<br>

### user_logs.csv
daily user logs describing listening behaviors of a user. Data collected until 2/28/2017.

 - msno: user id
 - date: format %Y%m%d
 - num_25: # of songs played less than 25% of the song length
 - num_50: # of songs played between 25% to 50% of the song length
 - num_75: # of songs played between 50% to 75% of of the song length
 - num_985: # of songs played between 75% to 98.5% of the song length
 - num_100: # of songs played over 98.5% of the song length
 - num_unq: # of unique songs played
 - total_secs: total seconds played

### members.csv
 user information. Note that not every user in the dataset is available.

 - msno
 - city
 - bd: age. Note: this column has outlier values ranging from -7000 to 2015, please use your judgement.
 - gender
 - registered_via: registration method
 - registration_init_time: format %Y%m%d
 - expiration_date: format %Y%m%d, taken as a snapshot at which the member.csv is extracted. Not representing the actual churn behavior.
