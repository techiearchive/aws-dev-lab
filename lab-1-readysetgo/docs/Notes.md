## Access the s3 bucket from ec2 instance

1. Create IAM policy to access the s3 bucket.
2. Create a IAM role and attache the policy.
3. Attach the IAM role with ec2 instance.
4. Access the bucket from ec2 instance and perform the s3 operations through command as well as code. 
5. Access s3 bucket through cli
  ```
  aws s3 ls
  ```
  To verify the credential
  ```
  aws sts get-caller-identity
  ```
