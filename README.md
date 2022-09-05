# Amazon_Vine_Analysis

## Overview of the analysis of the Vine program:
Analyzing Amazon reviews written by members of the paid Amazon Vine program.. 

## Results:
### Deliverable 1: Perform ETL on Amazon Product Reviews
* Step 1 - I picked the following dataset to analyse amazon reviews for beauty products
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Beauty_v1_00.tsv.gz
* Step 2 - Create a new database with Amazon RDS.
![image](https://user-images.githubusercontent.com/104685001/188505441-0dcd9af4-e9b2-4148-85bc-70ff159a448e.png)
* Step 3 - In pgAdmin, create a new database in your Amazon RDS server that you just create.
![image](https://user-images.githubusercontent.com/104685001/188505503-9699e40b-55aa-4675-ba95-53fb8946da91.png)
* Step 4 & 5 - Download the challenge_schema.sql file to your computer and run a query to create customers_table, products_table, review_id_table, and vine_table.
![image](https://user-images.githubusercontent.com/104685001/188505599-2cd49a11-91cf-4f51-8c1d-50bd9f8c3ad2.png)
* Step 6 & 7 - Download starter code and extract the review dataset to create a new dataframe.
![image](https://user-images.githubusercontent.com/104685001/188505752-80ec2c14-c126-4ad1-b49f-0548c8b8d96d.png)
* Step 8 - Transform the dataset into four DataFrames that will match the schema.
![image](https://user-images.githubusercontent.com/104685001/188505853-b45b5e22-153e-43aa-9279-1afece99f5ce.png)
![image](https://user-images.githubusercontent.com/104685001/188505862-83bd0430-a6fc-4c81-b21d-50e08740a510.png)
![image](https://user-images.githubusercontent.com/104685001/188505879-2a1e09c0-74ee-47b9-9c9a-df0668282710.png)
![image](https://user-images.githubusercontent.com/104685001/188505890-32799ffc-1602-4100-8e6d-727683cdc335.png)
* Step 9 - Loading into pgAdmin.
![image](https://user-images.githubusercontent.com/104685001/188505990-0d672bc7-5bc6-4f53-b564-062299c9495e.png)
![image](https://user-images.githubusercontent.com/104685001/188505998-d11c65b5-91cf-4dd1-9f61-76613c967a11.png)

### Deliverable 2: Determine Bias of Vine Reviews
* Step 1 - Filter the data and create a new DataFrame or table to retrieve all the rows where the total_votes count is equal to or greater than 20 to pick reviews that are more likely to be helpful and to avoid having division by zero errors later on.
![image](https://user-images.githubusercontent.com/104685001/188506100-83272906-1042-4de9-9414-30299544ba29.png)
* Step 2 - Filter the new DataFrame or table created in Step 1 and create a new DataFrame or table to retrieve all the rows where the number of helpful_votes divided by total_votes is equal to or greater than 50%.
![image](https://user-images.githubusercontent.com/104685001/188506161-f34a89bc-f06b-4da0-b5f9-b7bcce023285.png)
* Step 3 - Filter the DataFrame or table created in Step 2, and create a new DataFrame or table that retrieves all the rows where a review was written as part of the Vine program (paid), vine == 'Y'.
![image](https://user-images.githubusercontent.com/104685001/188506205-9f5d680e-e8b5-435d-88be-e18e154e1999.png)
* Step 4 - Repeat Step 3, but this time retrieve all the rows where the review was not part of the Vine program (unpaid), vine == 'N'.
![image](https://user-images.githubusercontent.com/104685001/188506244-67209956-feab-4e0a-a562-e1eabc3308bc.png)
* Step 5 - Determine the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review (paid vs unpaid).
![image](https://user-images.githubusercontent.com/104685001/188506282-7ceb905e-5380-457d-8392-61b1fa1cb09b.png)


##Summary:

The summary states whether or not there is bias, and the results support this statement (2 pt)
An additional analysis is recommended to support the statement (2 pt)
