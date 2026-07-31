# retail-etl-capstone
Databricks project
## Project Oveview 
This project demonstrate an end to end retail ETL pipeline build on databricks using the medallion architecture (Bronze,silver, Gold layer). The pipeline ingests retails data, transforms it using PySpark, store it in delta lake, Perform CRUD and merge operations, process streaming data using Auto loader, and provides business insight through sql dashboards.

--- 

### Architecture

CSV files
|
Bronze Layer (Raw Data)
|
Silver Layer ( Cleaned and Enriched Data)
|
Gold Layer ( Business Aggregations)
|
SQL Analytics Dashboard


---- 
#### Technologies Used

- DataBricks
- PySpark
- SQl
- Structured Streaming (Auto Ladder)
- Delta Merge
- Delta CRUD Operations
- DATABRICKS WORKFLOW
- Git and Github

##### Project Structure

~~~
retail-etl-capstone
|
|___notebooks
|   |__ 00_generate_data
|   |__ 01_Explore
|   |__ 02_bronze
|   |__ 03_silver
|   |__ 04_gold
|   |__ 05_CRUD
|   |__ 06_Streaming
|
|__ README>md
|__.gitignore
~~~


#### Medallion Architectue

### Bronze Layer 
 - Read raw CSV files
 - Performs Schema inference
 - Stores data as Delta tables

Tables:
- bronze_customers
- bronze_products
- bronze_orders

 ### Silver Layer
 - Cleans and transform data
 - joins customers, products and orders tables
 - calculated total revenue per order 

Tables:
- silver_enriched_orders

### Gold Layer

creates business - ready aggregated tables.

tables:
- gold_sales_summary
- gold_top_customers
-gold_region_sales

----

#### Delat lakes feature

Implemented the following Delat lakes operation:
- Read
- Insert
- Update
- Delete
- Merge (UPSERT)

#### Structured Streaming 

Implemented streaming using Auto Loader.

features:

- Cloudfiles
- Checkpointing
- Incremental Processing 
- Streaming into Delta Lakes

Streaming output table:
- Orders_stream

#### workflow

created a datbricks workflow to orchestrate the ETL pipeline
...
Bronze
|
Silver 
|
Gold
....

----

#### SQL analytics

Build SQL queries and visulalizations for:
- Total revenue
- Total Orders
- Revenue by Region
- Daily Sales Trend
- Top Customer

### Author 

*** ASAD HAQUE***

Big data Engineer
