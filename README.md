# M5_Forecasting_Accuracy
Kaggle competition: https://www.kaggle.com/c/m5-forecasting-accuracy  

Welcome to my first kaggle competition! It is a top 7% solution.  
Author: Yuman Lin and Shengjian Chen  

This is one of the two complementary competitions that together comprise the M5 forecasting challenge. The main goal of this M5 competition is to estimate the unit sales of Walmart retail goods.   


**Data**  
https://www.kaggle.com/c/m5-forecasting-accuracy/data  
calendar.csv - Contains information about the dates on which the products are sold.  
sales_train_validation.csv - Contains the historical daily unit sales data per product and store [d_1 - d_1913]  
sample_submission.csv - The correct format for submissions.   
sell_prices.csv - Contains information about the price of the products sold per store and date.  
sales_train_evaluation.csv - Includes sales [d_1 - d_1941] (labels used for the Public leaderboard)  

**Model**  
Core model: lightgbm  
Two ways:   
(1) different models according to different state_id (total 3 models, CA, TX and WI)  
(2) different models according to different store_id (total 10 models, CA_1, CA_2, CA_3, CA_4, TX_1, TX_2, TX_3, WI_1, WI_2, WI_3)  
I use the second way as my final submission because it performs better in my validation set.  

I only upload some of the notebooks but others are similar. You only need to change the store_id or state_id to train your data.  

**Evaluation**  
Weighted Root Mean Squared Scaled Error (RMSSE)  
https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/133834  
