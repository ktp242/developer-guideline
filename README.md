# developer-guideline
This is the guideline for naming classes,functions, isntances, applications, and documentations.

## AWS

### EC2 Load Balancer
The name should consists only alphanumeric characters. There should be no spaces in the name and use "-" to divide words. The name should has the VPC name as the first section. The second section should be the instances or the instance type that the load balancer stands in front of. Each section is divided with ":".

The name can not have more than 32 characters.

The load balancer should have a tag as "Target". Its value should be the URIs it listens to. Each URI is divided with ",".

### Internet Gateways
The name of an internet gateways should contain all lowercase characters and divide each words with "-". The name should be the VPC of the internet gateways that is attached to as the first section. If there are multiple internet gateways attached to a VPC, each internet gateways' name should contain a second section to indicates the particular purpose. Each section should be divided with ":".

### Lightsail Instance
The name should consists only alphanumeric characters. The name should contain 2 to 255 characters. There should be no spaces in the name and use "-" to break words.

The first section of the name should be the purpose of the application, for example, "blog", "database", "load-balancer".

Any naming section related to the application should have the type comes after the instance's name. It should be divided by "-" and be addressed as what it is. All the characters should be lowercase.

### Security Group
The "Security group name" should contains two sections. The first section shoud be the name of the VPC that the security group belongs to. The second section should be the type or purpose of the applications that are assigned in the security group. The sections are divided by ":". Each section should contain lowercase characters and devided with "-" if there are multiple words.

A security group should also has "Name". The way to name it should be the same as "Security group name".

Note that if the security group is the default security group of a VPC then the value in "Security group name" should just be "default" and the value in "Name" should be "<VPC name>:default".

The description should be a short sentence starts with the uppercase character in the first word.

A security group should have a tag named "Instance". The value should be the instances in the security group. Each instance should be divided with ",". Each of the instance in "Value" field should contain two sections. The first section is the type of the instance, and the second section is the name of the instance. We use ":" to divide the two sections.

### Subnet
The name consists of two sections. The first section should be the name of the VPC that this subnet belongs to. The second section should be the availability zone's last part. For example, it should be "1d" if the availability zone is "us-east-1d". The sections should be divided with ":". The name of each section should contain all lowercase characters and divide each words with "-".

### Tag
All the tags should be singular and start with uppercase. If a tag contains multiple words, it should be break in space and only the first word's first character should be uppercase.

If the format of a tag is a key-value set, only the first character of the key (Tag Name) is uppercase. If a key has multiple words, all the words are divided by single space.

The value of the tag consists mainly lowercase characters, unless it is the name of a person, a place, or a brand. The value can be a sentence with symbols (only the ones allowed by AWS). However, the length limit is 255 characters.

See, https://docs.aws.amazon.com/acm/latest/userguide/tags-restrictions.html

### Target Group
The name of the target group should be the type or the purpose that the group of instances share. It can contains two sections. The first section can be the type, and the second section can be the name. Sections are divied with ":". Each section contains all lowercase characters and divides each word with "-".

### VPC
The name of a VPC should contain all lowercase characters and divide each words with "-". The name should be the type or purpose of the applications that are designed in the VPC.

One of the excpetions is the "default" VPC. It has its special features in the AWS ecosystem so it is better to remain the name as "default".
