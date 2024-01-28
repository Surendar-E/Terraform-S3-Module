THe README.md file for AWS S3 BUCKET TERRAFORM MODULE

FEATURES:
               
Inputs 

1.Bucket_name: The name of the S3 bucket. Must be globally unique.
2.Tags: A map of tags to apply to the S3 bucket.
                  Outputs
1.Bucket_id: The ID of the created S3 bucket.
2.Bucket_arn: The Amazon Resource Name (ARN) of the S3 bucket.
           AWS resources created
1.aws_s3_bucket resource for the S3 bucket.
2.aws_s3_bucket_website_configuration resource for configuring the S3 bucket as a website.
3.aws_s3_bucket_acl resource for setting the S3 bucket access control.
4.aws_s3_bucket_policy resource for applying a bucket policy to control access.
                    USAGE
1.CLONE THE REPOSITORY:
 

        git clone 


2.configure the module:

Edit your Terraform Configuration file (main.tf) to include the module



	module "website_s3_bucket" {
	  source = "./modules/aws-s3-bucket"

	  bucket_name = "s3tfmoduleassignment"

	  tags = {
	    Terraform   = "true"
	    Environment = "dev"
	  }
	}



3.Apply The Configuration:

  Run the following commands:


          tofu init(terraform init)


          tofu plan(terraform plan)


          tofu apply(terraform apply)


4.clean up

when you no longer need the resources, run the below command:


        tofu destroy(terraform destroy)



          MODULE STRUCTURE

    -main.tf  
    -modules
        └── aws-s3-bucket
                ├── README.md
                ├── main.tf
                ├── outputs.tf
                ├── variables.tf
