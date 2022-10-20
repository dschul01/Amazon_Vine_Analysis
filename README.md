# Amazon_Vine_Analysis

Utilize PySpark, AWS RDS, and PGAdmin to analyze Big Data containing customer reviews.

## Purpose

The purpose of this project is to utilize PySpark, AWS RDS, and PGAdmin to analyze Amazon reviews on a select group of products and determine if there are any biases by members of the paid Amazon Vine program.  This program is a service wherein manufacturers and publishers pay a small fee to Amazon and provide products to Vine members in return for a published review.

One of fifty datasets containing specific product reviews is selected.  PySpark is used to run the dataset through the ETL (extract, transform, load) process connecting to an AWS RDS instance and load data into PGAdmin.  PySpark methods and functions are developed to analyze the dataset and determine bias levels by paid Vine members. 

## Results

The dataset utilized for this project contained reviews on watches.  Three questions needed to be addressed to assess whether there is bias from Vine members.  The calculations performed from the dataframes and results are included in the snapshot below. 

1) How many reviews were from Vine members and non-Vine members.
	* Vine review count:	    47		 
	* Non-Vine review count: 8,362	

2) How many Vine reviews were 5 stars and how many non-Vine reviews were 5 stars.
	* Vine 5-star review count:	     15		 
	* Non-Vine 5-star review count: 4,332	

3) What percentage of Vine reviews were 5 stars and the percentage of non-Vine reviews which were 5 stars.  
	* Vine 5-star review percent:	    32%		 
	* Non-Vine 5-star review percent: 52%	

![Calculations.png](https://github.com/dschul01/Amazon_Vine_Analysis/blob/main/Resources/Calculations.png)

## Summary

The results indicate there is no positivity bias for reviews on watches within the Vine program.  The volume of Vine reviews is nominal with 47 reviews compared to the population of 8,409.  Additionally, only 32% of those Vine reviews are 5 star compared to 52% from non-Vine members.

This project only analyzed reviews on one type of product.  Analysis should be performed on many, if not all of the product datasets to determine if Vine members are bias or not as a result of receiving free merchandise.  Furthermore, the project deliverable had the dataset filtered to reduce the overall population based on review's votes.  The excluded data should be analyzed to determine submission volume and ratings per Vine and non-Vine members. 
