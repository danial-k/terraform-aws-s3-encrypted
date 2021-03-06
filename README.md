S3 Encrypted bucket
===
Terraform module to create a server-side encrypted S3 bucket defaulting to public access block: ON.
Generates a random name if omitted.

# Examples
## Minimal with random name
```terraform
provider "aws" {
  version = "3.4.0"
  region  = "eu-west-2"
}

module "s3" {
  source  = "voquis/s3-encrypted/aws"
  version = "0.0.2"
}
```

## Custom name
```terraform
provider "aws" {
  version = "3.4.0"
  region  = "eu-west-2"
}

module "s3" {
  source  = "voquis/s3-encrypted/aws"
  version = "0.0.2"
  bucket  = "my-super-unique-bucket-name"
}
```
