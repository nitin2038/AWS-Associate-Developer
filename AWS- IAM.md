- [ ] IAM (Identity and Access Management) : Manage Users and their level of access to the AWS console.
- [ ] IAM is universal not regional, anything setup in IAM can viewed and utilized by any region.
- [ ] <strong>IAM Features</strong>
	- [ ] Centralized : Control of your AWS account
	- [ ] Access : Shared acess to your AWS account
	- [ ] Permissions : Granular Permissions
	- [ ] Identity Federation : Supports well known identity providers eg : FB, Linkedin
-<img src="https://github.com/nitin2038/AWS-Associate-Developer/blob/main/images/IAM_screenshot.png?raw=true" alt="iam extra features"/>

#### User , Roles and Groups
- [ ] USERS : Think People
- [ ] GROUPS : A collection of users under one set of Permissions
- [ ] ROLES : Create roles and assign to users, applications and services

##### IAM Policy
- [ ] A document that defines one or more permissions
- [ ] An IAM policy can be attached to a user, group or role.

- Each AWS resource has ARN (Amazon Resource Name ) which uniquely identifies it.
- example of S3 allAccess
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:*",
                "s3-object-lambda:*"
            ],
            "Resource": "*"
        }
    ]
}
```
- Only provide the permissions as least privilege ( **forces code to run with the lowest privilege/permission level possible**)