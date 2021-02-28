# cfn-init

## Hello-world

Create core stack
```bash

aws cloudformation deploy --stack-name hello-world-prep --template-file hello-world-prep.yaml

```
Obtain your S3 bucket
```bash

aws s3 ls

```
Send source code to S3
```bash

export BUCKET_NAME=hello-world-prep-sourcebucket-p4vyajcwtbg
aws s3 cp hello-world-flask.py s3://$BUCKET_NAME

```
Deploy app stack
```bash

aws cloudformation deploy --stack-name hello-world-app --template-file hello-world-app.yaml --capabilities CAPABILITY_IAM


curl hello-w-Elb-OWNXYVK2BZ7M-1315191116.us-east-1.elb.amazonaws.com

```

## LMNP

Deploy the stack
```bash
aws cloudformation deploy --stack-name lnmp --template-file lnmp-signal.yaml --parameter-overrides DBName=foo DBPassword=foobar123 DBRootPassword=barfoo321 DBUsername=bar
```