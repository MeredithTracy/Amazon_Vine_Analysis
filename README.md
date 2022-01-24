# Amazon Vine Analysis

## Overview of Analysis 
We have been tasked to run an analysis on Amazon reviews and looking into any potential bias in reviews from the Amazon Vine Program and regular reviews on various products. I chose to work with the pet products dataset. We will take our chosen dataset and run an ETL process then perform our analysis using PySpark. 

# Tools and Resources
Data: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Pet_Products_v1_00.tsv.gz
Analysis:PySpark
Tools: AWS RDS instances, Google Colab, and pgAdmin

## Results
![D2_Review_Counts](https://github.com/MeredithTracy/Amazon_Vine_Analysis/blob/main/Images/D2_Review_Counts.png)
The image above shows the code we used to answer the questions listed below. 

- How many Vine reviews and non-Vine reviews were there?
There are 170 Vine reviews and 37,840 non-Vine reviews. 

- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
Out of the 170 Vine reviews, 65 of them were 5 stars. For the 37,840 non-Vine reviews, 20,612 of them were 5 stars. 

- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
These numbers equate out to 38.235% for Vine reviews and 54.471% for non-Vine reviews. 

## Issues with Data
With the dataset I used for this analysis, I did run into some issues with duplicates. This would cause issues when trying to transfer the dataframes to PGAdmin. To correct this issue, I had to remove duplicates in each of my dataframes. Doing this fixed the error. The cause for this error likely sits within the dataset in regards to the ID columns in particular. 

## Summary
Based off the pet products dataset, there does not appear to be a positivity bias for reviews in the Vine program. If fact, they seem to be less likely to rate products 5 stars when compared to non-Vine reviews. There is a 16% difference when you look at the 5 star review percentages. 

I think it would be important to look at the full breakdown of reviews from 5 stars to 0 stars to see if there is potential for a negative bias for Vine reviews. I also think it is important to look at more than just one dataset. Just because there isn't a positivity bias for pet products, does not mean that trend stands for all products on Amazon. This data is too specific to make that comparison. Also, because this dataset has potential issues with duplicates, it would be critical to expand our data. 
