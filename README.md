# serverless
Writing serverless applications using AWS lambda 

# Important Commands

# 0. Initial setup and config (one-time)
serverless config credentials --provider aws --key <key> --secret <secret> --profile <IAM Admin User Name>

# 1. Create a new template project using serverless
sls create --template aws-python3 --path python-example-project

# 2. Deploy the serverless project
sls deploy -v

# 3. Deploy just the function (not working with docker)
sls deploy function -f hello-iam-example

# 4. Remove everything created by sls within a project
sls remove

# 5. Invoke a function with logs on cmd
sls invoke -f hello-iam-example -l

# 6. Check streaming logs via CLI (-t is for tail)
sls logs -f hello-iam-example -t

# 7. Installing serverless plugins
sls plugin install --name serverless-python-requirements