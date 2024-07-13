# Home Sales Analysis Overview
This project leverages SparkSQL to analyze home sales data, focusing on metrics like average home prices. We used Spark to create temporary views, partition data, and explore the benefits of caching for performance optimization.

# Tools Used
- Apache Spark: For powerful data processing and analytics.
- PySpark: The Python interface for Apache Spark, enabling seamless data manipulation.
- SparkSQL: To execute SQL queries on Spark dataframes.
- Jupyter Notebook: For interactive code development and execution.

# Key Metrics
- Four-Bedroom Prices: Average prices for four-bedroom houses per year.
- Three-Bedroom, Three-Bathroom Prices: Average prices for these homes per construction year.
- Specific Criteria Prices: Average prices for homes with three bedrooms, three bathrooms, two floors, and at least 2,000 square feet.
- Prices by View Rating: Average prices for homes with a view rating, priced over $350,000, including query runtime.

# Data Preparation and Analysis
The home sales data from home_sales_revised.csv was read into a Spark DataFrame, and a temporary table named home_sales was created for SQL queries. To enhance performance, the home_sales table was cached, reducing the query runtime from 0.85 seconds to 0.34 seconds. The data was also partitioned by date_built and stored in Parquet format, resulting in a query runtime of 0.77 seconds. Finally, the home_sales table was uncached, and the uncaching process was verified using PySpark.

This analysis demonstrated effective data handling and performance optimization in SparkSQL, providing valuable insights into home sales metrics and the impact of caching and partitioning on query performance.

# Results
## Uncached runtime

## Cached runtime

## Parquet format (partitioned by date_built)
