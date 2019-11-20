# outputs_skills_map_tf
This Repo contains TF example for outputs


## What do outputs do
Terraform outputs is a function you can use to get information about a resource you have created
i.e. 

```
output "public_ip" {
	value = "${aws_instance.example.public_ip}"

}
```

here we are using the resource variable `${aws_instance.example.public_ip}` to get the information about our instance from the AWS API. The information is parsed to us at the end of executing our code i.e. 

```
Outputs:

public_ip = 3.134.76.210
```
## How to use this repository
In this repository there is a file called main.tf, that creates a single aws instance and at the end of the creation process outputs the public DNS and IP.

To use this file you need to have AWS account and Terraform installed
When you have the files saved localy do `terraform init` in the folder that main.tf resides, after the provider plugins are downloaded do `terraform plan` to see what will change  and if everything seems in order do `terraform apply`

At the end you will get the output with the created instances' IP and DNS
