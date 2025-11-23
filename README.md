<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | 6.20.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_archive"></a> [archive](#provider\_archive) | 2.7.1 |
| <a name="provider_aws"></a> [aws](#provider\_aws) | 6.20.0 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_cloudwatch_log_group.lambda_json_to_csv_log_group](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/cloudwatch_log_group) | resource |
| [aws_glue_job.json_to_csv](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/glue_job) | resource |
| [aws_iam_policy.glue_policy](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/iam_policy) | resource |
| [aws_iam_policy.lambda_policy](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/iam_policy) | resource |
| [aws_iam_role.glue_role](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/iam_role) | resource |
| [aws_iam_role.lambda_role](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/iam_role) | resource |
| [aws_iam_role_policy_attachment.attach_lambda_policy_to_lambda_role](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/iam_role_policy_attachment) | resource |
| [aws_iam_role_policy_attachment.glue_role_policy_attachment](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/iam_role_policy_attachment) | resource |
| [aws_lambda_function.json_to_csv_lambda](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/lambda_function) | resource |
| [aws_lambda_permission.s3_lambda_invoke_permission](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/lambda_permission) | resource |
| [aws_s3_bucket.this](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/s3_bucket) | resource |
| [aws_s3_bucket_acl.s3_acl](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/s3_bucket_acl) | resource |
| [aws_s3_bucket_lifecycle_configuration.this](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/s3_bucket_lifecycle_configuration) | resource |
| [aws_s3_bucket_notification.lambda_trigger](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/s3_bucket_notification) | resource |
| [aws_s3_bucket_ownership_controls.this](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/s3_bucket_ownership_controls) | resource |
| [aws_s3_bucket_policy.this](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/s3_bucket_policy) | resource |
| [aws_s3_bucket_public_access_block.this](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/s3_bucket_public_access_block) | resource |
| [aws_s3_bucket_server_side_encryption_configuration.this](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/s3_bucket_server_side_encryption_configuration) | resource |
| [aws_s3_bucket_versioning.this](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/s3_bucket_versioning) | resource |
| [aws_s3_object.python_pyspark_script](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/resources/s3_object) | resource |
| [archive_file.lambda_function_zip](https://registry.terraform.io/providers/hashicorp/archive/latest/docs/data-sources/file) | data source |
| [aws_caller_identity.current](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/data-sources/caller_identity) | data source |
| [aws_iam_policy_document.glue_policy_document](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/data-sources/iam_policy_document) | data source |
| [aws_iam_policy_document.glue_trust_policy_document](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/data-sources/iam_policy_document) | data source |
| [aws_iam_policy_document.this](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/data-sources/iam_policy_document) | data source |
| [aws_region.current](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/data-sources/region) | data source |
| [aws_s3_bucket.s3_bucket](https://registry.terraform.io/providers/hashicorp/aws/6.20.0/docs/data-sources/s3_bucket) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_access_key"></a> [access\_key](#input\_access\_key) | n/a | `string` | n/a | yes |
| <a name="input_archive_retention_noncurrent_days"></a> [archive\_retention\_noncurrent\_days](#input\_archive\_retention\_noncurrent\_days) | n/a | `string` | `90` | no |
| <a name="input_aws_account_id"></a> [aws\_account\_id](#input\_aws\_account\_id) | The AWS account ID to deploy resources | `string` | `"211125325120"` | no |
| <a name="input_cw_logs_retention_period_days"></a> [cw\_logs\_retention\_period\_days](#input\_cw\_logs\_retention\_period\_days) | Cloudwatch Logs Retention Period in Days | `number` | `3` | no |
| <a name="input_default_retention_noncurrent_days"></a> [default\_retention\_noncurrent\_days](#input\_default\_retention\_noncurrent\_days) | n/a | `string` | `180` | no |
| <a name="input_env"></a> [env](#input\_env) | value representing the environment (e.g., dev, staging, prod) | `string` | `"sbx"` | no |
| <a name="input_glue_job_name"></a> [glue\_job\_name](#input\_glue\_job\_name) | Name of the Glue job to start | `string` | `"json_to_csv"` | no |
| <a name="input_lambda_function_name"></a> [lambda\_function\_name](#input\_lambda\_function\_name) | Name for the Lambda function | `string` | `"json-to-csv-lambda"` | no |
| <a name="input_lambda_runtime"></a> [lambda\_runtime](#input\_lambda\_runtime) | Runtime for the Lambda function | `string` | `"python3.13"` | no |
| <a name="input_name"></a> [name](#input\_name) | value representing the name of the S3 bucket | `map(string)` | <pre>{<br/>  "s3_first_bucket_name": "bkt01-source-json-data",<br/>  "s3_second_bucket_name": "bkt02-destination-csv-data",<br/>  "s3_third_bucket_name": "bkt03-pyspark-src-code"<br/>}</pre> | no |
| <a name="input_project"></a> [project](#input\_project) | Project name | `string` | `"json-to-csv-etl-datapipeline"` | no |
| <a name="input_region"></a> [region](#input\_region) | The AWS region to deploy resources in | `string` | n/a | yes |
| <a name="input_secret_key"></a> [secret\_key](#input\_secret\_key) | n/a | `string` | n/a | yes |
| <a name="input_tags"></a> [tags](#input\_tags) | n/a | `map(string)` | `{}` | no |
| <a name="input_token"></a> [token](#input\_token) | n/a | `string` | n/a | yes |
| <a name="input_versioning"></a> [versioning](#input\_versioning) | n/a | `string` | `"Disabled"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_cloudwatch_log_group_arn"></a> [cloudwatch\_log\_group\_arn](#output\_cloudwatch\_log\_group\_arn) | n/a |
| <a name="output_first_bucket_arn"></a> [first\_bucket\_arn](#output\_first\_bucket\_arn) | n/a |
| <a name="output_glue_job_arn"></a> [glue\_job\_arn](#output\_glue\_job\_arn) | n/a |
| <a name="output_glue_job_name"></a> [glue\_job\_name](#output\_glue\_job\_name) | n/a |
| <a name="output_glue_policy_arn"></a> [glue\_policy\_arn](#output\_glue\_policy\_arn) | n/a |
| <a name="output_glue_role_arn"></a> [glue\_role\_arn](#output\_glue\_role\_arn) | n/a |
| <a name="output_lambda_function_arn"></a> [lambda\_function\_arn](#output\_lambda\_function\_arn) | n/a |
| <a name="output_lambda_function_name"></a> [lambda\_function\_name](#output\_lambda\_function\_name) | n/a |
| <a name="output_lambda_iam_policy_arn"></a> [lambda\_iam\_policy\_arn](#output\_lambda\_iam\_policy\_arn) | n/a |
| <a name="output_lambda_iam_role_arn"></a> [lambda\_iam\_role\_arn](#output\_lambda\_iam\_role\_arn) | n/a |
| <a name="output_s3_bucket_names"></a> [s3\_bucket\_names](#output\_s3\_bucket\_names) | Map of S3 bucket ids keyed by bucket resource key |
| <a name="output_second_bucket_arn"></a> [second\_bucket\_arn](#output\_second\_bucket\_arn) | n/a |
| <a name="output_third_bucket_arn"></a> [third\_bucket\_arn](#output\_third\_bucket\_arn) | n/a |
<!-- END_TF_DOCS -->