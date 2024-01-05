What is DynamoDB?

Amazon DynamoDB is a fully managed NoSQL database service provided by Amazon Web Services (AWS). It is designed to deliver fast and predictable performance at any scale. DynamoDB offers a flexible schema-less data model, allowing you to store and retrieve data using simple key-value or document-based operations.

Steps to create a table &import data from s3 and scan and query and export into s3

Step 1: Creating a DynamoDB Table.
![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/8f4624b1-d62d-4a16-9cc5-c97b1fd68fe1)

•	Click Create Table

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/3598fa11-88b2-4145-b40a-fb72bf4f472a)

 
•	In Table detail, input table name, partition key, and sort key.

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/9ec2adc0-6926-4697-9aee-a9f53d03e15c)

 
•	Then click Create Table

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/47e8dc6a-cf78-49a9-81c3-c28daedd4905)


•	 

•	The table will appear in the DynamoDB tables list. Wait a short while for the status table to change to active if it is initially still developing.
•	

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/57f2f773-a49c-4bf4-a831-d969408513cd)

•	 
•	Go to Explore items: your-table-name, select 'Create item'

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/be720b64-09a2-4f4d-b5a8-baeffb207ae7)




 
•	Enter the value for the table attribute, and then select "Create item" to add data to the table.


![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/49984311-afd5-4314-b468-95e5c69e508f)

 
•	It will be displayed like this.

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/4d7cc240-7653-4db9-a88e-7afbba8dd143)


 



STEP2: Importing Data from a CSV File.

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/a17b907f-012c-431a-8321-118b29467325)


•	Select DynamoDB from the menu, click Import from S3, and then select "Import from S3" to import datasets from an S3 bucket. 


•	 
•	Before anything else, I suggest uploading your CSV into s3 first. so you just need to browse it. Choose the format based on the first .
•	
•	 ![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/2c4d9c03-3ce7-4ebd-ad14-fcaabc2b1a40)

After that, fill in the table details, by inputting your table name and its primary key. *I change the file name to Saipavantable. 

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/b229a9a1-4551-41f7-994a-87e340abb94e)

 
In the table setting, I choose the default setting. 

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/a460394b-e30d-4b33-b4b5-d76e2a033e11)

 
•	Then on the review and import page, when you see that all the data is in accordance with what you wish for, click.

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/38a5732c-7628-4a28-8aa8-e73030fb3c7f)

•	
•	 
•	It will take the file for a while to import, as can be seen in the status.

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/ba125bcb-a92d-42e3-b2dc-e015ffd578df)

•	 
•	We will wait until we have a green 'Completed' status beside the imported data.

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/e8390c3e-619b-4d7d-bf08-7a71b821c902)

 

•	When the file finished importing, we can see it by going back to the DynamoDB menu > Tables > Click our table > explore table item.
![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/3d4da4d0-c09a-49b3-a46c-6c8b77012316)

 
•	This is the table that we just imported.



Step 3: Performing Queries or Scans with Filters.

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/569f639c-5337-4588-9ac1-7e93c81db6e5)

 
Scan Data.
Click on Explore Item and scan. You can explore this function yourself.
![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/0faf3279-8fbc-4a67-9dbd-d56754b2463d)

 
Query:
Click the query options on the same page as the last one. And explore the function ourselves.
![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/7c630f96-60fe-48e0-8a92-e683c6fc2176)
![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/435af475-929e-4c31-8fab-59b680c0fa0e)



 


 
Step 4: Exporting Results from DynamoDB
•	The last step is to export the data. First, we need to go to DynamoDB > Export to S3.

![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/632b44e6-07dc-488c-9679-45c589501c38)

•	 

•	Input your source table, and the destination bucket that you want to export it into > Export.
![image](https://github.com/saipavankapisetti/AWS-DYNAMO-DB-DOCUMENTATION/assets/121307495/5772affe-a54e-494e-ac5d-14509bcd1586)


 
•	We will wait until we have a green 'Completed' status beside the exported data.
•	Then we will go to S3 > our bucket that we export our data in > and we will see our exported data as 'AWSDynamoDB/'.




