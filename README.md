# aws-glue-hudi-cdc

Repository to deploy sample pipeline which demonstrate CDC using AWS Glue 


## Create Glue Connector for Hudi via Console

* Create Glue connector and connection for Hudi as described in [blog](https://aws.amazon.com/blogs/big-data/writing-to-apache-hudi-tables-using-aws-glue-connector/)

## Deploy the infrastructure

hudi_connection_name=

```sh
aws cloudformation deploy --stack-name aws-glue-with-hudi-cdc \
   --template-file infra/cf/HudiConnectorCFn.yml \
   --parameter-overrides HudiConnectionName=${hudi_connection_name} \
   --capabilities CAPABILITY_NAMED_IAM
```

## Bibliography

* [writing-to-apache-hudi-tables-using-aws-glue-connector](https://aws.amazon.com/blogs/big-data/writing-to-apache-hudi-tables-using-aws-glue-connector/)
