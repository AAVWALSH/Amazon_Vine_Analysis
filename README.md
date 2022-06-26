# Amazon_Vine_Analysis
Big Data using PySpark, Amazon Web Service (AWS), Google Colaboratory, and pgAdmin

### Overview

The purpose of this analysis is to explore one of Amazon's product datasets to determine if there is any bias towards favorable reviews when they are part of the paid Vine program. This is important for both Amazon and the product producers to know as it could lead to false reviews and a possible negative customer experience if they get a product that isn't as good as expected as it had bloated positive reviews the companies paid for. 
To complete this analysis I performed the ETL process to extract the dataset from Amazon's AWS, transofrm the dataset, connect it to an AWS RDS instance, and then loaded the data in pgAdmin. I then used PySpark to determine the bias in the data. For this projuct I specifically used the dataset gathered on pet products as I've personally given far too much money to Amazon on behalf of my dog. 

### Results

- How many Vine reviews and non-Vine reviews were there?

![image](https://user-images.githubusercontent.com/100727593/175835942-8b9e111a-ceb2-4308-9fd0-32a7510b4411.png)

There were a total of 2,643,619 reviews overall. In order to narrow the analysis we filtered the data where the percentage of 'helpful' votes was greater than 50%. Of these 170 votes were paid for through the Vine program and 37,840 were not. 

- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

![image](https://user-images.githubusercontent.com/100727593/175836185-30df3515-b858-43fb-ae8a-03def9b962f5.png)

There was a total of 1,645,553 5 star reviews. 65 of the 5 star reviews were paid for. 20,612 of the 5 star review were not paid for. 

- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

![image](https://user-images.githubusercontent.com/100727593/175836227-cfc3abf5-b01b-42fe-9081-1175d3022e06.png)

35% of the 5 star reviews were paid for. 54% of the 5 star reviews were not paid for. 

### Summary

Based on the fact that 54% of the 5 star reviews, among the reviews deemed 'helpful', were not paid for indicatess that there is not a bias towards favorable paid reviews. Only 35% of the paid reviews were 5 stars which may indicate that paid reviewers responded honestly about the products, and that they may be good but not great. For further analysis I would look at the breakdown of the other star ratings. It would be interesting to see if there were any paid 1 star rating. 
Looking at the product titles column, it is clear that this dataset covers a wide range of pet products. For a more accurate analysis of the Vine program might be to look at a select number of best-selling products that were included in the Vine program and compare the ratio of paid/unpaid reviews on those select product. 
