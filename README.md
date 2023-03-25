Mongo vs Cassandra Vs HBase

https://logz.io/blog/nosql-database-comparison/

```
Source comes from a msql db which is a rdbms.

We'll be reading data using spark and we'll do all sort of ETL trnslations
and we'll be loading the data to hive

Lets say we're loading data from table A and data will be loaded at table A1.

Finally downstream will be using A1 table fo all their reporting purposes.

Lets say we need to load another table B and need to do a lookup with A1 which is loaded at hive at spark.

In this case hive might be slow

Even if we do performance optimization like partioning, lookup is not optimized .

HBase is very very faster compared to respective lookups and upserts 

HBase will internally update the previous record.

We can have a copy of A1 completely for lookups such that B can lookup using A1 at Hbase and not at hive.
```

<img width="996" alt="Screenshot 2023-03-25 at 2 14 48 PM" src="https://user-images.githubusercontent.com/43849911/227707106-9d8f3ecc-5f91-4a0f-96f8-4638750bbd82.png">
