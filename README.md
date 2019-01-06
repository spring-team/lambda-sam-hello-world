# lambda-sam-hello-world
Lambda SAM hello world

```
export BUCKET=com.atomist.hello

export STACK_NAME=lambda-sam-hello

aws s3 mb s3://$BUCKET

[/Users/rodjohnson/Library/Python/3.7/bin/]sam package --template-file template.yml --s3-bucket $BUCKET --output-template-file packaged-template.yml

sam deploy --template-file packaged-template.yml --stack-name $STACK_NAME --capabilities CAPABILITY_IAM
```
