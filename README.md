# Azure_Data_Factory

1. TOMTOM API traffic data from an on-premises Sql server is imported into an Azure SQL database.
2. A data flow is created, this takes the data from the Azure SQL database and goes through multiple tranformations.
3. The transformed data is then exported to a final table in the Azure SQL database.


Data Flow (Data Transformation staging table to new table in SQL Azure DB)
![image](https://user-images.githubusercontent.com/66565804/210152281-bd017fe1-9e06-4937-ae2b-6a3d95359a4b.png)


Data Pipeline (Copy data from on premise SQL Server to SQL Azure DB, Transform and export to new table in SQL Azure DB)
![image](https://user-images.githubusercontent.com/66565804/210152319-96124572-7bbc-44f9-bb38-290d50807e08.png)
