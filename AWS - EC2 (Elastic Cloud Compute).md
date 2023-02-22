#### Introducing EC2
What is EC2 ?
- [ ] Secure resizable compute capacity in cloud.
- [ ] Like a VM,only hosted in AWS instead of your own data center.
- [ ] The capacity you want when you need it.
- [ ] We are in complete control of our ec2 instances.

#### EC2 pricing options
- [ ] On Demand 
- Pay by the hour or second depending on the type of instance you run, great for flexibility
- [ ] Spot
- Purchase unused capacity at discount of up to 90% , grate for flexible start , end times
- [ ] Reserved
- Reserved capacity of 1-3 years, 72% discount on hosurly charge, great if we have fixed requirements.
- [ ] Dedicated
- Great for server bound-licenses to reuse or compilance requirements.

### EBS (Elastic Block Store) 
- Storage Volumes that you can attach to your EC2 instances. (like disk in our local computer)
- When EC2 instances is launched first it has 1 EBS volume.
- Types :
	- gp2, gp3, io1(provisioned iops ssd), io2
 - [ ] The volume created needs to be in the same availabilty zone as that of the EC2 instance.

### Elastic Load Balancer
-   Distributes network traffic across a group of servers.
- If a website gets really popular, we can add more web server register them with load balancer and load balancer will start sending traffic to our new webserver as well.
- | load balancer type | Description |
|-------------------|--------------|
| Application load balancer | HTTP and HTTPS (used for load balancing HTTP/HTTPS traffic, operate at layer 7 and are application aware)(We can route request depending on header as it operates at layer 7) |
| Network load balancer | TCP and high performance (used where extreme performance is required, layer 4) |
| Classic load balancer (legacy) | HTTP , HTTPS and TCP |

#### 7 layer Model :
- A conceptual framework which describes the functions of a network.
 ![[./images/7layer_screenshot.png]]


##### X-forwarded-for Header  
- Identify the originating IP address of a client connecting through a load balancer.
![[laodBalancer_screenshot.png]]

#### Route 53
- [ ] It is Amazon's DNS service
- [ ] Allows you to map a domain name that you own to
-   EC2 instances
-   Load Balancers
-   S3 Buckets

```
Route53 ---> LoadBalancer ---> EC2 instance
```

### AWS CLI
- [ ]  aws configure to use the aws cli
- [ ] aws configure list shows your aws configuration like below```

```
      Name                    Value             Type    Location
      ----                    -----             ----    --------
   profile                <not set>             None    None
access_key     ****************tink shared-credentials-file
secret_key     ****************lear shared-credentials-file
    region                us-east-1      config-file    ~/.aws/config
```

eg : aws s3 list (list s3 bucket)
```
aws s3 mb s3://new49r0939040 (make s3 bucket with name new49r0939040 )
- echo "hey" > hello.txt
- aws s3 cp hello.txt s3://new49r0939040 (copies hello.txt file to our bucket)
```