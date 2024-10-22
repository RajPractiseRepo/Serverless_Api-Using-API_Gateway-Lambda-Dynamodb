# Building a Serverless API on AWS: Writing and Querying Data with API Gateway, Lambda, and DynamoDB

![serverless-flow-diagram](https://github.com/user-attachments/assets/eeafb10d-6eb0-430c-a2eb-31283467422a)


# Project Summary

💡Our goal is to **create a powerful serverless API that interacts with DynamoDB to perform CRUD operations** \
and supports additional operations for testing.

💡The API will be backed by an AWS Lambda function, which will handle incoming requests and interact with the DynamoDB table based on the payload. This project aims to showcase how to build a scalable and cost-efficient serverless API using AWS services.


# Technologies Used

 •	**Amazon API Gateway** \
 •	**AWS Lambda** \
 •	**AWS DynamoDB** \
 •	**AWS IAM** \
 •	**Advanced Rest Client**

 # Project Architecture
The project consists of three main components:
1.	**Amazon API Gateway:** Serves as the frontend for the API, routing HTTP requests to the appropriate Lambda function. 
2.	**AWS Lambda:** A Lambda function acts as the backend, handling various operations and interacting with the DynamoDB table.
3.	**DynamoDB:** The NoSQL database service stores data, and I create a table with a primary key for efficient data retrieval.


![image](https://github.com/user-attachments/assets/e794f376-1a15-4314-8f75-3668cee872f5)


# Prerequisites
Before starting, make sure you have the following prerequisites: \
•	An AWS account with appropriate permissions to create Lambda functions, API Gateway, and DynamoDB. \
•	AWS CLI installed and configured with your AWS credentials.


# Steps to Build the API
Follow these steps to build the CRUD serverless API: 
1.	**Set up DynamoDB Table:** \
o	Go to the AWS Management Console and open the DynamoDB service. \
o	Create a new table with the desired name and primary key configuration. \
o	Configure any additional settings as per your requirements.

![dynamodb-aws](https://github.com/user-attachments/assets/a117ca00-24e5-4837-a8b9-262f07fa09fd)

2.	**Create Lambda Functions:** \
o	Go to the AWS Management Console and open the Lambda service. \
o	Create a new Lambda function for each CRUD operation (create, read, update, delete). \
o	Configure the function's runtime and permissions to access DynamoDB.

![lambda-function-aws](https://github.com/user-attachments/assets/e79265a5-8a31-4cce-b141-fc9d3fffbee9)



3. 	**Implement Lambda Function Code:** \
o	Write the code for each Lambda function, implementing the respective CRUD operation. \
o	Use the provided code snippets as a starting point and modify them according to your table structure.

![lambda_function](https://github.com/user-attachments/assets/b07fc79c-81dc-488f-95c2-7dd2148c4a83)

4.	**Create IAM role for allow configuration for lambda to interact with Dynamo DB:**
o Attach policy DynamoDb Access to the role.


5.	**Create API Gateway:** \
o	Go to the AWS Management Console and open the API Gateway service. \
o	Create a new REST API. \
o	Configure API Gateway resources and methods for each CRUD operation. \
o	Integrate the methods with the corresponding Lambda functions.

![api-gateway](https://github.com/user-attachments/assets/165ab44c-1f36-47e0-bbd0-21a77105c3c6)

6.	**Deploy API:** \
o	Deploy the API in API Gateway to make it accessible. \
o	Test the API endpoints using the Invoked provided URL using **Advanced Rest Client**.

# PUT Request:
![put_request](https://github.com/user-attachments/assets/acdf5237-d3fb-4818-a049-3b4a905b6cac)

# Record got added in DynamoDB Table:
![dynamodb](https://github.com/user-attachments/assets/fb1c4a6e-1101-4178-b147-6ab311a89d38)


# GET Request:
![get_rqeuest](https://github.com/user-attachments/assets/a5bfcac1-54ed-49f3-a37f-ca53046660fe)

# Note: Similarly other CRUD Operations like POST, DELETE, PATCH can be implemented.













