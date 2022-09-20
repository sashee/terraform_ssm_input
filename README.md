# Example code for how to use sensitive inputs in Terraform using SSM Parameters

## Use

* Create an SSM parameter with ```type: SecureString``` and an arbitrary value:

![image](https://user-images.githubusercontent.com/82075/191213381-30d4b579-43ed-4d49-86a5-4eb4cca547c4.png)

* ```terraform init```
* ```terraform apply```
* Input the name of the parameter (```secret_token``` in the above example)
* Go to the resulting URL
* The Lambda function gets the name of the token and also permission to read it (not implemented)

## Cleanup

* ```terraform destroy```
* Delete the SSM parameter
