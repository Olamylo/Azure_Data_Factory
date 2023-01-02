# Azure_Data_Factory Pipelines

1. Copy data from on premise SQL Server to SQL Azure
TOMTOM API traffic data from an on-premises Sql server is imported into an Azure SQL database.
A data flow is created, this takes the data from the Azure SQL database and goes through multiple tranformations.
The transformed data is then exported to a final table in the Azure SQL database.


Data Flow (Data Transformation staging table to new table in SQL Azure DB)
![image](https://user-images.githubusercontent.com/66565804/210152281-bd017fe1-9e06-4937-ae2b-6a3d95359a4b.png)


Data Pipeline (Copy data from on premise SQL Server to SQL Azure DB, Transform and export to new table in SQL Azure DB)
![image](https://user-images.githubusercontent.com/66565804/210152319-96124572-7bbc-44f9-bb38-290d50807e08.png)


2. Get_Table_List_And_Trigger_Copy_Data
This pipeline uses a look up activity in Azure data factory to select all the tables in an on-premesis database,
it then triggers pipeline 3(Iterate_and_copy_multi_tables_onpremsql_to_azuresql). 


![image](https://user-images.githubusercontent.com/66565804/210273608-123b94c9-55e9-4145-a314-68851cb4ab2b.png)


3. Iterate_and_copy_multi_tables_onpremsql_to_azuresql
this uses a ForEach activity and iterates over all the list of tables obtained from the on-premesis database and copies each table to Azure SQL database.


![image](https://user-images.githubusercontent.com/66565804/210273645-e6c91e94-2e3a-4a52-8bfd-81cee39c6395.png)
