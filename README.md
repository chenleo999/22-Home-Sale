# 22-Home-Sale

completed by Li Chen, 6/14/2024

description:
This is a practice of SparkSQL on home sales data, which include temp view creation, data partition, cache and un-cache temp table followed by verification.


Steps:
1. import PySpark SQL
2. read csv into Spark DataFrame
3. create a temp table
4. run sql query to find out avg price by each build year for houses with
    a. 4-bed 
    b. 3-bed, 3-bath 
    c. 3-bed, 3-bath, 2-flr and >=2000 sqft 
5. run sql query to find out avg price by view rating for houses with >= $350,000, query runtime 1.64 sec
6. cache temp table and confirm success
7. run same query in step 5 with cache data, query runtime 1.24 sec, a bit faster than un-cached 
8. partition by "date_built" on the formatted parquet home sales data
9. generate temp table for the parquet 
10. run same query in step 5 and 7, query runtime 2.14 sec, somewhat longer than above 2
11. uncache temp table and confirm

