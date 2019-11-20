# outputs_skills_map_tf
This Repo contains TF example for outputs


## What are TF outputs
Terraform outputs is a peace of code you can use to get information about a resource you have created
i.e. 

```
output "public_ip" {
	value = "${aws_instance.example.public_ip}"

}
```

here we are using the resource variable `${aws_instance.example.public_ip}` to get the information about our instance from the AWS API. The information is the parsed to us at the end of executing our code i.e. 

```
Outputs:

public_ip = 3.134.76.210
```
