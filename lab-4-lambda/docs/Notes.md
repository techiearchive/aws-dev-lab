## AWS lambda trigger a lambda function when objects are uploaded into s3 bucket and lambda function will calculate the max, min and avg of the numbers available in s3 object.

1. Create a s3 bucket name "calculator-input-(your-name)"
2. Upload a file with random numbers eg: [numbers.txt](https://github.com/techiearchive/aws-dev-lab/blob/master/content/numbers.txt)
3. Create a role with name "lambda_execution_role" and attach below policies
    - AmazonS3ReadOnlyAccess
    - AWSLambdaBasicExecutionRole
4. Go to Lambda service in AWS management console and create function
5. Choose "Author from scrach" and fill the basic information
    - Function name: JavaCalculator
    - Runtime: Java 11 (Corretto)
    - Permissions: Use Existing role -> "lambda_execution_role"

6. Click create funciton
7. Now update Runtime settings. Handler: com.amazonaws.lambda.Calculator
8. Go to Funciton overview click Add trigger
9. Under trigger configuration choose s3.
10. Then choose bucket that already created "calculator-input-(your-name)"
11. Event type: All object create events
12. Click Recursive innovation acknowledge and click add.
13. Now Java code is prepared for below operations
    - Respond to an Amazon S3 event in Lambda.
    - Retrieve a file from s3 bucket.

14. To test the code locally execute CalculatorTest.java with junit.
15. Before execute Junit there is a JSON payload file src/test/resources/s3-event.put.json, Need to update the bucket name with "calculator-input-(your-name)"
16. Output will be min, max and avg number.

[AWS Lambda lab](https://github.com/techiearchive/aws-dev-lab/blob/master/lab-4-lambda/images/lab-4-lambda.png)
