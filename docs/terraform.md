## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| admin_name | Name for the admin group and role (e.g. `admin`) | string | `admin` | no |
| admin_user_names | Optional list of IAM user names to add to the admin group | list | `<list>` | no |
| attributes | Additional attributes (e.g. `policy` or `role`) | list | `<list>` | no |
| delimiter | Delimiter to be used between `namespace`, `stage`, `name`, and `attributes` | string | `-` | no |
| enabled | Set to false to prevent the module from creating any resources | string | `true` | no |
| namespace | Namespace (e.g. `cp` or `cloudposse`) | string | - | yes |
| readonly_name | Name for the readonly group and role (e.g. `readonly`) | string | `readonly` | no |
| readonly_user_names | Optional list of IAM user names to add to the readonly group | list | `<list>` | no |
| stage | Stage (e.g. `prod`, `dev`, `staging`) | string | - | yes |
| switchrole_url | URL to the IAM console to switch to a role | string | `https://signin.aws.amazon.com/switchrole?account=%s&roleName=%s&displayName=%s` | no |
| tags | Additional tags (e.g. map(`BusinessUnit`,`XYZ`) | map | `<map>` | no |

## Outputs

| Name | Description |
|------|-------------|
| group_admin_arn | Admin group ARN |
| group_admin_id | Admin group ID |
| group_admin_name | Admin group name |
| group_readonly_arn | Readonly group ARN |
| group_readonly_id | Readonly group ID |
| group_readonly_name | Readonly group name |
| role_admin_arn | Admin role ARN |
| role_admin_name | Admin role name |
| role_readonly_arn | Readonly role ARN |
| role_readonly_name | Readonly role name |
| switchrole_admin_url | URL to the IAM console to switch to the admin role |
| switchrole_readonly_url | URL to the IAM console to switch to the readonly role |

