# Serverless-DynamoDB-Lambda-API


### Step 1: Create a DynamoDB Table
1. Open the AWS Management Console and navigate to the DynamoDB service.
2. Click on the "Tables" section and then select "Create Table."
3. Provide a name for your table, define the primary key, and configure any additional settings.
4. Click "Create Table" to initiate the table creation.

### Step 2: Create a Lambda Function
1. Go to the AWS Lambda console.
2. Click on "Create Function" and choose "Author from Scratch."
3. Provide a name for your Lambda function, select a runtime (e.g., Node.js, Python), and set up the execution role.
4. Open index.mjs in the console's code editor, and replace its contents with the index.mjs provided
6. Save and deploy your Lambda function.

### Step 3: Create an HTTP API
1. Navigate to the AWS API Gateway console.
2. Click on "Create API" and select "HTTP API."
3. Provide a name for your API and click "Create API."
4. Note the API endpoint URL generated after creating the API.

### Step 4: Create Routes
1. In the API Gateway console, go to the "Routes" section.
2. Add routes for each CRUD operation (e.g., GET, POST, PUT, DELETE).
3. Define the resource paths and methods for each route.

### Step 5: Create an Integration
1. Within each route, create an integration with AWS Lambda.
2. Link the corresponding Lambda function to each route's integration.

### Step 6: Attach Your Integration to Routes
1. Associate the integrations you created with their respective routes.

### Step 7: Test Your API
To make sure that your API is working, we use curl
To get the URL to invoke your API Choose your API.
Note your API's invoke URL. It appears under Invoke URL on the Details page.



Now, when you invoke your HTTP API, API Gateway will route the requests to your Lambda function, which interacts with DynamoDB. Ensure that your IAM user has the necessary permissions for Lambda, DynamoDB, and API Gateway to avoid any access issues.
