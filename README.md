# **Amazon_Vine_Analysis**

## Project Overview

### Executive Summary
In this module, Amazon customer reviews were analyzed to determine if there were any biases between Vine paid vs. non-paid members’ reviews.
To accomplish this analysis, a series of [review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) were available for this analysis.  In this analysis, the home entertainment dataset was used to extract, transform and load data into a DataFrame.

### Data Sources
[Home Entertainment Dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Home_Entertainment_v1_00.tsv.gz)

### Software Used
PySpark 
pgAdmin (postgres 14.5)
Google Colab (2022/9/30 release)

<br>

## Results 

### Deliverable 1

The Home Entertainment dataset was extracted as a DataFrame:

| ![Figure1](https://github.com/mrmarken/Amazon_Vine_Analysis/blob/main/Images/1-01-dataframe.png) |
| :---: |
| **Figure 1.** DataFrame Extracted from AWS |


All four tables were successfully created and subsequently uploaded onto pgAdmin: 

| ![Figure2](https://github.com/mrmarken/Amazon_Vine_Analysis/blob/main/Images/1-02_customer_id_table.png) | ![Figure3](https://github.com/mrmarken/Amazon_Vine_Analysis/blob/main/Images/1-03-product_id_table.png) | 
| :---: | :---: |
| **Figure 2.** Customer_id Table | **Figure 3.** Product_id Table |

| ![Figure4](https://github.com/mrmarken/Amazon_Vine_Analysis/blob/main/Images/1-04-review_id_table.png) | ![Figure5](https://github.com/mrmarken/Amazon_Vine_Analysis/blob/main/Images/1-05-vine_id_table.png) | 
| :---: | :---: |
| **Figure 4.** Review_id Table | **Figure 5.** Vine_id Table |

### Deliverable 2

Five DataFrames were successfully created using PySpark on Google Colabs:

| ![Figure6](https://github.com/mrmarken/Amazon_Vine_Analysis/blob/main/Images/2-01-total_votes.png) |
| :---: |
| **Figure 6.** Total Votes |

| ![Figure7](https://github.com/mrmarken/Amazon_Vine_Analysis/blob/main/Images/2-02-votes_above_50.png) |
| :---: |
| **Figure 7.** Votes Where `helpful_votes` divided by `total_votes` is >= 50%  |

| ![Figure8](https://github.com/mrmarken/Amazon_Vine_Analysis/blob/main/Images/2-03-paid_votes.png) |
| :---: |
| **Figure 8.** Total Paid Votes |

| ![Figure9](https://github.com/mrmarken/Amazon_Vine_Analysis/blob/main/Images/2-04-unpaid_votes.png) |
| :---: |
| **Figure 9.** Total Unpaid Votes |

| ![Figure10](https://github.com/mrmarken/Amazon_Vine_Analysis/blob/main/Images/2-05-reviews_total.png) |
| :---: |
| **Figure 10.** Reviews Totals |


<br>

### Deliverable 3: A Written Report on the Analysis

* How many Vine reviews and non-Vine reviews were there?
  * As seen in figure 10 (above), it can be summarized that there are 261 Paid vs 24,040 unpaid votes

* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
  * In the dataset, there are 106 Paid vs 10,899 unpaid 5-star reviews.

* What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
  * The percentage of Vine (paid) members was 40.6% vs. 45.3% of non-Vine (unpaid) members

### Summary

Based on the results, it can be summarized that Vine members did not show bias in their ratings as the percentages of 5-star ratings are fairly comparable to unpaid (non-Vine) members.

To further support these findings, it is recommended that a few more of the available datasets is examined using similar methods.  Additionally, it may be helpful to include an analysis of the complete data (rather than filtering out some data points).

