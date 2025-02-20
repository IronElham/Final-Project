# Final-project

**Introduction:** 

Business case: As a freelancer consultant, I offer detailed analysis to firms who are seeking to improve their business strategies and product portfolio to be future proof. In this specific project, I have consolidated detailed analysis from Sephora dataset, a beauty and cosmetic retailer. It is French multinational retailer of personal care and beauty products, offering around 340 brands. 

For the purpose of this project, the target variable ‘is_recommended ’in Sephora dataset is selected. This variable shows whether the user or the author of product review, recommends the product or not. 

Problem statement: Which factors influence probability of getting deal from the investors?

Hypotheses:

H0: There is significant association between is_recommended and skin_tone.

H1: There is significant association between secondary_categroy and skin_tone.

H2: There is significant association between is recommended and brand name.

H3: The mean of original usd price is not equal to the value price (discount price).

H4: At least one category has a significantly different mean rating.

H5: At least one skin type has a significantly different mean price.

**Data preparation and cleaning:**

Total of 4 dataframe for review and 1 data frame for product info was obtained from Kaggle data source.  The data contained 48 columns, where unnecessary columns are dropped for the purpose of this project. Data cleaning techniques used for dropping unnecessary columns, duplicates, null values, fillna, changing data types
For more specific information on cleaning data please refer to the Jupyter Notebook in the repo

**Findings:**

H0: Is_recommened and skin_tone: Reject the null hypothesis, there is significant association between is_recommended and skin_tone, where the effect size is small. 

H1: Secondary_category and skin_tone: Rejected the null hypothsis, There is significant association between secondary_categroy and skin_tone, where the effect size is small. 

H2: Is_recommended  and brand name: Reject the null hypothesis, There is significant association between is recommended and brand name, where the effect size is small. 

H3: Original Price and Value price: Reject the null hypothesis, The mean of original usd price is not equal to the value price (discount price), where the effect size is small. 
Although the result from Wilcoxon Signed-Rank test statistic shows small p value and statistically significant difference (rank of the prices are consistently different), the log scale does not show much difference. 
Calculated mean difference between 2 variables, -0.54 is insignificant, thus there is not a meaningful difference between prices.

H4: Rating and Secondary_category: Reject the null hypothesis, At least one category has a significantly different mean rating, where the effect size is medium. 

H5: Original Price and skin type: Reject the null hypothesis, At least one skin type has a significantly different mean price, where the effect size is medium. 


**More analysis:**

1.	Multicollinear between variables total_deal_amount and price_usd_y and value_price_usd 0.99, price_use_y and sales_price_usd , value_price_usd and sales_price_usd, total_feedback_count and total_pos_feedback_count, total__pos_feedback_count, reviews and love_count 0.82, total_neg_feeback_count and rating_x, sephora exclusive and price_usd_x, sephora exclusive and price_usd_y, sephora exclusive and value_price_usd, sephora exclusive and sales_price_usd, loves_count and price_usd_y, loves_count and sales_price_usd, loves_count and online_only , loves_count and value_price_usd, rating_y and helpfulness

2.	Machine learning techniques, to train feature `skin_tone`, `rating_y` ,`total_pos_feedback_count`, `loves_count`, `hair_color`, `skin_type`, `eye_color`, `reviews`, `rating_x`, `sales_price_usd`,`brand_name_x`, `product_name`,`secondry_category`, `variation_type`, `variation_desc`,`online_only`,`out_of_stock`, `new`, `limited_edition to predict is_recommended (target variable). 

3.	Across all different ML models, as the is_recommened dirstribution is imbalancd, techniques of undersampling with TomeLinks and Oversampling with SMOTE  has been used. The has resolved the issue of imbalanced data and improved models’ scores. 

4.	XGBoost model has the highest overall score for precision, recall, F score and accuracy. 

5. Sentiment analysis of Vader and RoBERTa as Natural Language Processing techniques has been conducted to extract the emotions and the sentiment scores from the review of the consumers. Overall the review_text revealed positive sentiment score for VADER and Joy emotional mood or customer satisfaction from RoBERTa. 

*For further information please refer to the Jupyther notebooks, presentation and Tableau on this repo.
