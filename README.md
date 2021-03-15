# Amazon_Vine_Analysis by Ketaki
## Overview of the analysis:
The purpose of this analysis is to determine if there is any bias towards favorable reviews from Vine members in the Amazon Vine [**Software**](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Software_v1_00.tsv.gz) reviews dataset. This is achieved by the use of PySpark and performing the ETL process to -
1. Extract the dataset
2. Transform the data
3. Load the transformed data to pgAdmin by connecting to a RDS instance of AWS.
## Results: 
After performing the ETL process on the dataset, we found that -
- There were **1,23,748** reviews in total, out of which **255** were Vine reviews and **1,23,493** were Non-Vine reviews.
- ![Vine Reviews](https://github.com/ketpradh/Amazon_Vine_Analysis/blob/main/Resources/Vine%20Reviews%20set.PNG)
- ![Non-Vine Reviews](https://github.com/ketpradh/Amazon_Vine_Analysis/blob/main/Resources/Non-Vine%20Reviews%20set.PNG)
- ![](https://github.com/ketpradh/Amazon_Vine_Analysis/blob/main/Resources/Reviews%20Total%20result%20set.PNG)
- Out of the total **72,836** 5 star reviews, there were **102** Vine reviews that were 5 stars and **72,734** non-Vine reviews that were 5 stars.
- **40%** of Vine reviews were 5 stars whereas **~59%** of non-Vine reviews were 5 stars.

## Summary: 
- Based on the results, we find that there was higher percentage(59%) of 5 stars reviews from non-Vine reviewers than from Vine reviewers(40%) which indicate that **there was no positivity bias for reviews in the Vine program.** If there was a positivity bias, then, the percentage of 5 star non-Vine reviews would have been higher than what we found(40%)
- ![Results Image](https://github.com/ketpradh/Amazon_Vine_Analysis/blob/main/Resources/Reviews%20Total%20result%20set.PNG)
- We can also check the **verified_purchase** column that can tell us if the reviewers actually purchased the product before giving the review.
- However, to be more sure of things, we can also perform a negativity bias for reviews in the Vine program. Are Vine users less likely to provide a negative review than the non-Vine users? This can be done by finding the number of 1-star or 2-star reviews in both the categories. 
