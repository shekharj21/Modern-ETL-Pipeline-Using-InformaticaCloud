# Modern-ETL-Pipeline-Using-InformaticaCloud

# 1. System Architecture :
![Screenshot (522)](https://github.com/shekharj21/shekharj21/assets/54074505/ccf40928-5595-4309-affc-2f2d86e614dc)

# 2. Uploading a data to Amazon S3 :
- Create a S3 Bucket.
![Screenshot (523)](https://github.com/shekharj21/shekharj21/assets/54074505/8fc4badd-94a3-46cd-a9b8-4edabc66c2ce)

- Add Customer.Csv File in it.
![Screenshot (524)](https://github.com/shekharj21/shekharj21/assets/54074505/c9707f6a-421a-4073-a480-a34a02171e83)

# 3. Create a PostgreSQL in AWS RDS:

- Keep the Public Access ON
- Giver initial Database name as "ordersdb"
![Screenshot (525)](https://github.com/shekharj21/shekharj21/assets/54074505/f753896a-0717-4437-8d37-90a8a3121263)


# 4. Download PGadmin

- Download Pg admin and connect to S3 PostgreSQL.
- Use Endpoint, Port number, Db name, Username and Password.

# 5. Setup Informatica Cloud Account

# 6. Add S3 Coonection
- Open Informatica Cloud
- Add connection for S3
- Add Access Key
- Add Secret Key
![Screenshot (526)](https://github.com/shekharj21/shekharj21/assets/54074505/3bbf081c-cce3-4bee-86d8-c36a1336e417)


# 7. Add Postgre Connection

# Create Customer Destination and Order Destination in PostgreSQL (Data Warehouse)
- This step is needed because we need destination (data Warehouse ) to drop the data from S3 and PostgreSQL. 
-Create the Schema for vendor.customer
- Create Schema for order.operation
- create mapping with S3 source to Postgres Destination (vendor.customer)
- Create mapping with postgreSQL to Destination (operations.order)

# 8.Add Mapping for Souce and Destination
- Source : S3
- Destination : PostgreSQL
