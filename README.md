# Amazon_Vine_Analysis by Ketaki
## Overview of the analysis: Explain the purpose of this analysis.
The purpose of this analysis is to determine if there is any bias towards favorable reviews from Vine members in the Amazon Vine [**Music**](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Music_v1_00.tsv.gz) reviews dataset. This is achieved by the use of PySpark and performing the ETL process to -
1. Extract the dataset
2. Transform the data
3. Load the transformed data to pgAdmin by connecting to a RDS instance of AWS.
## Results: Using bulleted lists and images of DataFrames as support, address the following questions:
After performing the ETL process on the dataset, we found that -
- How many Vine reviews and non-Vine reviews were there?
- There were 4,751,577 reviews in total, out of which 1933 were Vine reviews and 4749607 were Non-Vine reviews.
- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
- Out of the total 3290473 5 star reviews, there were zero Vine reviews that were 5 stars and 67,580 non-Vine reviews that were 5 stars.
- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

## Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
- Based on the results, we find that there were more 5 stars reviews from non-Vine reviews than Vine reviews which indicate that there was no positivity bias for reviews in the Vine program. 
- ![Results Image]()
- We can also check the **verified_purchase** column that can tell us if the reviewers actually purchased the product before giving the review.
- However, to be more sure of things, we can also perform a neagtivity bias for reviews in the Vine program. Are Vine users less likely to provide a negative review than the non-Vine users? This can be done by finding the number of 1-star or 2-star reviews in both the categories. 
