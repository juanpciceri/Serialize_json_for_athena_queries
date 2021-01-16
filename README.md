# Serialize_json_for_athena_queries
This lambda function will convert a regular not serialized json, impossible for use with AWS Athena queries into a serialize json, able to be used with lambda.
The lambda is trigger every time a file is upload to an S3 bucket, read the body of the file and transform the json into a serialized formed -one single line-.

For this lambda to work is neccessary to configure the correct trigger and role for the lambda function.
