# Cloudindoio
FACE REKOGNITION USING AMAZON REKOGNITION

Creating an android based application.
Upload images to the AWS from android:
This will help you with  how to create an S3 bucket in AWS, how to get  all the credentials to upload images to that bucket from an android device and  to get the image URL   for the further use.
What is this all about?
These are the prerequisites to upload the image file to the AWS S3 bucket from the android mobile.
Prerequisites:
•	AWS S3 bucket
•	AWS access key Id
•	AWS secret access key
•	AWS server region
•	Android studio
To get the prerequisites follow the instructions:
AWS bucket:
To get the AWS bucket first you have to log in to the amazons website then you have to create the bucket  just going into S3 then we have a option to create bucket..
	 Now create your bucket with the name you want.
	 After creating the bucket create the folder inside the bucket if needed.
	Here after creating bucket you can upload files.
AWS access key Id and AWS secret access key:
	To get the the access key and secret key, on the top right side of the navigation bar you will find the user name with the down arrow mark click on it and select the security credentials.
	After selecting the security credentials select the Access Keys (Access Key ID and Secret Access Key) option.
	Then create new access key were you will get the server access key and id  on clicking the show access key and copy that and also secret access key.
AWS region:
The region in which the AWS S3 bucket is created, the same region should be provided in the app also. In our case the region is US-EAST_1.
Mobile side Implementation:
The code for android app is given in the folder “Android application”. Download the folder and open it in “android studio” software.


AWS LAMBDA FUNCTION IN AMAZONS ACCOUNT FOR IMAGE REKOGNITION

Follow the steps in this section to create a simple Lambda function.
To create a Lambda function
	Sign in to the AWS Management Console and open the AWS Lambda console.
	Note that AWS Lambda offers a simple Hello World function upon introduction under the How it works label and includes a Run option, allowing you to invoke the function as a general introduction. This tutorial introduces additional options you have to create, test and update your Lambda functions, as well as other features provided by the Lambda console and provides links to each, inviting you to explore each one in depth.
Choose Create a function under the Get Started section to proceed.
	The console shows the Get Started page only if you do not have any Lambda functions created. If you have created functions already, you will see the Lambda > Functions page. On the list page, choose Create a function to go to the Create function page.
	On the Create function page, you are presented with two options:
	Author from scratch
	Blueprints
	In Author from scratch, do the following:
	In Name*, specify your Lambda function name.
	In Runtime*, leave the default python 2.7
	In Role*, leave the default Choose an existing role.
	In Existing role*, choose lambda_basic_execution.
	Choose Create Function.
	Under your new function-name page, choose the Add triggers panel, you can optionally choose a service that automatically triggers your Lambda function by choosing one of the service options listed. In our case we chose to S3.
	After the successful creation of the function Invoke the Lambda Function Manually and Verify Results in cloudwatch Logs.
	AWS Lambda executes your function on your behalf. The handler in your Lambda function receives and then processes the sample event.
	Upon successful execution, view results in the console.
Showing the output to mobile using DynamoDB
	Create the ProductCatalog Table
	Open the DynamoDB console at https://console.aws.amazon.com/dynamodb/.
	Choose Create Table.
	In the Create DynamoDB table screen, do the following:
	In the Table name field, type ProductCatalog.
	For the Primary key, in the Partition key field, type your field name, and set appropriate Data Type..
	When the settings are as you want them, choose Create.
	Now, whenever an image file is uploaded to aws s3 bucket using the mobile app it dynamically triggers the lambda function and the results are shown in cloudwatch logs.
	The lambda function is initiated and rekognition is done.
