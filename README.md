Quick Steps:

1- Create 3 containers for Redis, MariaDB, and Kafka using Docker Compose with the spark-docker.yml file

Script 1: code_00_03_Spark_BDE_Setup_Prerequisites.ipynb
This script would help with establishing connections with MariaDB, Redis, and Kafka

Script 2: code_03_XX_Spark_BDE_Batch_Data_Engg.ipynb
This script would walk you through the ETL pipeline for Batch processing. We extract the data from the source database using the parallelism capabilities of Spark, and store it in an HDFS like location, then consolidate the data and push it into the main central MariaDB. 

Script 3: code_04_04_Spark_BDE_Build_a_streaming_analytics_job.ipynb and code_04_04_Spark_BDE_Build_a_streaming_analytics_job
These scripts build a Real-time ETL PySpark pipeline using Kafka. Events are generated mimicking a real-time simulation. A Kafka producer and Consumer are used to publish and subscribe to the data in the form of messages. Spark is used to transform that incoming stream of data, perform some aggregations, and store the results in Redis and MariaDB. 

Finally, two more exercise files combine the real-time and batch pipelines processing to form a kind of hybrid ETL pipeline.
