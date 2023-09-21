# Amazon Electronics Reviewer Value 
This is the repository for Camaron Mangham and Vinu Lakkur's Milestone 1 Project | University of Michigan School of Information | Master of Applied Data Science

This Milestone focuses on data manipulation and data exploration.

## Background
Our goal was to assess “reviewer lifetime value” and larger trends in spend volume by analyzing reviews of Amazon purchases. The Amazon reviews dataset contains 233.1 million reviews across all categories of product, so we will only focus on a subset of the electronics category, which only contains about 6.7 million records (the full electronics dataset contains almost 21 million records). The results of such analysis could provide insight into the characteristics of different customer groups that leave reviews for items. This information could also be compared and contrasted with other groups of customers such as those that do not leave reviews. In a business setting, such information could be valuable in order to determine how much business effort to put toward either capturing or communicating with certain sets of reviewers/customers. Overall, the motivation for this analysis is inspired by the common practice of determining customer lifetime value (CLV) to understand customer segments and build customer relationships[3-4], and a desire to apply big data and data mining concepts.


## Key Findings and Challenges
- Storing this large data in memory was not viable, and required the leveraging of distributed data processing via PySpark.
- Compressed files must be decompressed to take advantage of distributed processing via PySpark.
- A majority of the reviews are from 2014-2017 which marks a period of rapid growth for Amazon.
- Median spending by reviewers is around $11 on average. Further analysis could be performed regarding price category and review count correlation. 
- Information about a reviewers first Amazon review gives us marginal predictive value regarding their Lifetime Value as a Reviewer
- Initial analysis suggests there is potential for further feature engineering and modeling to yield higher, - and more useful, predictive ability 

## Keywords 
Consumer Behavior, Product Reviews, Amazon Electronics, Customer Lifetime Value, Big Data, Predictive Value


## Data Sources
The datasets, derived from a dataset of Amazon product reviews developed by researchers at UC San Diego, available as compressed JSON files via download at: https://nijianmo.github.io/amazon/index.html:

- Amazon Electronics Reviews 5-core (4.19 GB JSON): Contains 6,739,590 user reviews from 1999 to 2018. These data have been reduced to extract the k-core, such that each of the remaining users and items have k reviews each 
- Amazon Electronics transaction metadata (11 GB JSON): Includes descriptions, price, sales-rank, brand info, and co-purchasing links for 786,868 products.

## Using these notebooks
This project was built in MacOS and Windows OS. Dependencies are recordes as *environment.yml* (Mac environment) and *requirements.txt* (Windows environment). 

Data samples are provided for reference (first 100 rows of both original sets and the dataset engineered for analysis), but it will be necessary to download the original files to replicate the notebooks in their entirety.
