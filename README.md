# Serialize_json_for_athena_queries

As you probably know, AWS athena let you use SQL queries with files stored in S3, nevertheless if you want to avoid problems or not having any result at all while using AWS athena for this purpose, you must have files with proper format. For example, not serialized json files are not able to be queried with ATHENA, this lambda fixes that issue. Converting json files into one single line format using a serverless approach with AWS lambda.

This lambda function will convert a regular not serialized json, impossible for use with AWS Athena queries into a serialize json, able to be used with AWS Athena queries.
The lambda is trigger every time a file is upload to an S3 bucket, read the body of the file and transform the json into a serialized formed -one single line-.

For this lambda to work is neccessary to configure the correct trigger and role for the lambda function.
