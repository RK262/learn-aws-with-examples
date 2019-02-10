# Now to create S3 bucket using Cloudformation , we are using AWS CLI command to create Stack.
# In the below example , we have passed template body as json and also required parameters (if necessary.)
# First example is for creating only S3 bucket and it will use CreateSampleS3Bucket.json as input.
aws cloudformation create-stack --stack-name your-test-stack --template-body file://CreateSampleS3Bucket.json --parameters ParameterKey=pNewBucketName,ParameterValue=my-test-s3-bucket-name-aws-s3

# Second example is to create S3 bucket which takes CreateS3BucketWithBucketProperties.json as input and also the paramters are :
# 1. pNewBucketName = "Name of your bucket."
# 2. pEnvironment = "dev"
# 3. pResourceCreator = "test-user"
aws cloudformation create-stack --stack-name your-test-stack --template-body file://CreateS3BucketWithBucketProperties.json --parameters ParameterKey=pNewBucketName,ParameterValue=my-test-s3-bucket-name-aws-s3 ParameterKey=pEnvironment,ParameterValue=dev ParameterKey=pResourceCreator,ParameterValue=my-test-user
