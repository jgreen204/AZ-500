# Intro into Cloud Computing

- > IaaS
   - > Infrastructure as a Service - Only pay for the infra you use
- > PaaS
   - > Platform as a Service
   - > When you don’t really know what you require, you still need to look after the underlying assets, but not the provisioning of it
- > SaaS
   - > Focus on the Software itself
- > FaaS
   - > Function as a Service

> # Introduction to AWS

> Regions and Availability Zones

- > Regions are spread across the globe
   - > Ohio, North Carolina, London, Paris, Bahrain, Tokyo, Sydney for example
- > Availability zones are areas within each region
   - > North, South, East and West - ap-southeast-2b may be Sydney North availability zone for example. BUT, these naming conventions are randomly generated for each user to stop them always using ‘A & B’ availability zones.

# Security and Identity

> ## Data Protection

- > *Amazon Mazie* * Discover and protect your sensitive data
- > *AWS Key management service* * Store and manage encryption keys
- > *AWS CloudHSM*
   - > Hardware based key storage
- > *AWS Certificate manager*
   - > Provision, manage and deploy SSL & TLS security certificates
- > *AWS Secrets manager*
   - > Rotate, manage and retrieve secrets

> ## Infrastructure Protection

- > *Amazon Guard Duty*
   - > Automatically detect threats
- > *Amazon Inspector*
   - > Analyse application security
- > *AWS Config*
   - > Record and evaluation configurations of your AWS Records
- > *AWS Cloud Trail*
   - > Track use and activity and API Usage

> ## Identity Management

- > *AWS IAM*
   - > Securely manage access to AWS account services and resources
- > *AWS Single Sign-On*
   - > Implement cloud single sign-on
- > *Amazon Cognito*
   - > Manage identity inside applications
- > *AWS Directory Services*
   - > Implement and manage Microsoft Active Directory
- > *AWS Organisations *
   - > Centrally govern and manage multiple AWS account in one place

> ## AWS Identity and Access Management (IAM)

- > Manage who can access what in your AWS accounts
- > Create Users and Groups
- > Allow or deny via policies
- > Free service in all AWS accounts
- > Each user has a User ARN - Amazon Resource Name
- > Within the JSON Code an Asterix “*” next to ‘Resource’ will mean they have access to ALL resources along with the ‘Effect’ set to “Allow”
- > When you change from ‘Allow’ to ‘Deny’ this is known as an Explicit Deny, so will override any other Allow that the user is granted in any other policy.
- > Least privileged security is best policy

> ## AWS Secrets Manager

- > Protect the secrets required to a access your resources
- > Rotates automatically
- > Stores passwords, keys and tokens
- > You can request your password from secrets manager from within your code

> ## AWS Directory Service

- > Managed Microsoft Active Directory
- > Managed Simple Active Directory
- > AD Connector - Allows users to logon to their AWS accounts with their AD account
- > Distributed service with automatic failover
- > Compatible with other AWS Services

# Consider Compute

> ## Instances - Virtual Machines

- > Amazon Elastic Compute cloud
   - > Secure and resizeable virtual machines in the cloud
- > Amazon EC2 Spot
   - > Run fault tolerant workloads at 90% off the normal price
- > Amazon EC2 Auto Scaling
   - > Automatically add or remove capacity based on demand
- > Amazon Lightsail
   - > An easy-to-use platform to build applications and websites

> # Containers

- > Amazon ECS
   - > Run secure, and scalable containers
- > Amazon ECR
   - > Store, manage and deploy container images
- > Amazon EKS
   - > Fully managed Kubernetes service

> # Serverless

- > AWS Lambda
   - > A compute service to run code without servers

> # Edge

- > AWS Outposts
   - > Run AWS Services on-premise
- > AWS Snow family
   - > Bring your data into the cloud using an actual truck to carry all your HDDs
- > AWS Wavelength
   - > Access AWS services via 5G network's
- > VMWare Cloud on AWS
   - > Migrate VMWare workloads
- > AWS Local Zones
   - > Run latency sensitive application closer to end users

> # Exploring EC2

- > Elastic Compute Cloud
   - > Rent virtual computers
   - > Choose from various types with differing CPU, RAM and Storage
   - > Different optimisations are available as well
   - > Pay by the hour or the second
   - > Instant upgrade possibilities - turn off the VM and upgrade then turn back on - On Demand pricing
- > Multitenancy
   - > Host machine has EC2 intances underneath it. EC2 instances are not aware of one another, they are secure and seperate.
- > EC2 instance types:
   - > **General Purpose**
      - > Provide a balance of compute, memory, and networking resources. You can use them for a variety of workloads, such as:
         - > application servers
         - > gaming servers
         - > backend servers for enterprise applications
         - > small and medium databases
   - > **Compute Optimised instances**
      - > IIdeal for compute-bound applications that benefit from high-performance processors. Like general purpose instances, you can use compute optimized instances for workloads such as web, application, and gaming servers.
   - > **Memory Optimised Instances**
      - > Designed to deliver fast performance for workloads that process large datasets in memory
   - > **Accelerated Computing Instances**
      - > These use hardware accelerators, or coprocessors, to perform some functions more efficiently than is possible in software running on CPUs. Examples of these functions include:
         - > Floating-point number calculations
         - > Graphics processing
         - > Data pattern matching
   - > **Storage Optimised Instances**
      - > Designed for workloads that require high, sequential read and write access to large datasets on local storage. Examples of workloads suitable for storage optimized instances include:
         - > Distributed file systems
         - > Data warehousing applications
         - > High-frequency online transaction processing (OLTP) systems

> # Clarifying Containers

- > Create a package of your program

> # Learning Lambda

- > Serverless Compute
- > Runs your programming code in response to events
- > Runs your code for you “somewhere”
- > Charged by the milliseconds
- > Price depends on RAM use

> # Studying Storage

- > File based storage
- > Block Storage - broken up into equal size - common use in DB servers and email servers
- > Object storage - stored in objects and given a unique identifier and are stored in a flat memory model

> ## File Storage

- > Amazon Elastic File Service (EFS)
   - > A scalable, elastic and cloud native Network file system
- > Amazon FSx for Windows File Server
   - > A fully managed file storage for Windows Server.

> ## Block Storage

- > Amazon EBS
   - > Easy to use, high performance block storage

> ## Object Storage

- > Amazon S3
   - > Store and  retrieve any amount of data from anywhere in the world

> ## Backup

- > Centrally manage and automate backup across AWS Services

> ## Data Transfer

- > AWS Storage Gateway
   - > Provide on-premises access to unlimited cloud storage
- > AWS DataSync
   - > Easily transfer data to and from AWS up to 10 times faster than normal
- > AWS Transfer family
   - > Transfer files to Amazon S3 using SFTP, FTP and FTPS

> # Amazon Simple Storage Service (S3)

- > Object storage service
- > Have the Object ID you can access the file
- > Industry Leading Durability - 99.99999999999% (11 9s)
- > Storage Classes
   - > S3 Standard
   - > S3 Standard infrequent
   - > S3 Datazone Infrequent
   - > S3 Glacier
   - > S3 Glacier Deep Archive
   - > S3 Intelligent Tiering

> S3 Glacier

- > Data archival and long-term backup
- > $1/TB/Month
- > Query-in-place functionally
- > Three retrieval options:
   - > Standard - low cost
   - > Bulk retrieval - cost effective for large amount of data
   - > Expedited - urgent retrieval

> ## Amazon Elastic Block Store (EBS)

- > Enables redundancy within an AZ
- > Allows users to take snapshots of it data
- > Offers encryption of its volumes
- > Volume types;
   - > General purpose SSD - Cost effective type designed for general workloads
   - > Provisioned IOPS SSD - High performance volume for low latency apps
   - > Throughput Optimised HDD - Designed for frequently accessed data
   - > Cold HDD

> # Explaining Elastic File System (EFS)

- Lets you connect 2 file servers across the network with your Linux EC2 Servers
- Multiple servers can access the file system at the same time
- Highly available and durable - spread over different zones
- Storage classes:
   - Standard
   - Infrequent access
- Automatically grows and shrinks with the amount of data stored in it
- Encrypted

> # AWS Storage Gateway

- Gives you access to virtually unlimited cloud storage on premises
- File Gateway
   - Gives you SMB and NFS interfaces to S3
- Tape Gateway
   - Presents a virtual tape library on your local network
- Volume Gateway
   - Presents an iSCSI block storage volume to your on-premise applications

> ## AWS Snowball & Snowmobile

![Screenshot 2023-10-15 at 20.38.21.jpeg](https://res.craft.do/user/full/f14daadb-9175-da55-3d5f-ffa67ffaaf79/1A34E3CA-D6F1-41F8-83CD-8AA55DF5333A_2/sNYN1WwU0ATjnczu120t5Nd7qc0kTtINhrG1fAqny8Iz/Screenshot%202023-10-15%20at%2020.38.21.jpeg)

# Defining Databases

- > More than 15 different DB types
   - > Relational
   - > Key-value
   - > In-memory
   - > Document
   - > Graph
   - > Time Series
   - > Wide Column
   - > Ledger

> ## Relational Databases

- > Amazon Aurora
   - > A mySQL and PostgreSQL compatible database built for the cloud
- > Amazon RDS - PaaS - Fully managed
   - > Easily set up, use and scale multiple database engines

> ### Amazon Redshift

- > Relational DB
- > A cloud data warehouse
- > Petabyte scale
   - > High performance disks and columnar storage
   - > offers the ability to fully encrypt contents
   - > Provides isolation with a VPC
   - > Enables querying exabytes of data in Amazon S3 using Redshift Spectrum

> ## Key-value Database

- > Amazon DynamoDB
   - > Fast and reliable NoSQL DB for any scale

> ## In-Memory Databases

- > Amazon ElastCache
   - > Managed, in-memory data store service for Redis and memcached.

> ## Document DB

- > Amazon DocumentDB
   - > MongoDB compatible, fast, scalable, highly available document database.

> ### Amazon Database Migration Service (DMS)

- > Enables you to move data into AWS from existing databases
- > Supports both continual and one time migration of data
- > Supports many popular commercial and open source databases
- > Only pay for compute leveraged in the migration process

> # Reviewing Relational Database Service (RDS)

- > Stores data that is related to each other
- > Database Engines
   - > MySQL
   - > MariaDB
   - > Microsoft SQL Server
   - > PostgreSQL
   - > Oracle
   - > Amazon Aurora
- > Amazon RDS
   - > Easy to set up
   - > Fully managed
   - > Scalable - use across availability zones
   - > Automated backups
   - > Automatic host replacement

> # Discussing DynamoDB

- > NoSQL DB Service
- > Key-value document DB
- > Single-digit millisecond performance
- > Data within the DB doesn’t have to match
- > Fully managed
- > Works in multiple regions
- > Built in security, back up and restore
- > Can handle more than 20,000,000 requests per second
- > Works great with serverless
- > works great with mobile applications
- > Examples of use cases:
   - > Advertising
   - > Gaming
   - > Retail
   - > Banking
   - > Software
   - > Media
   - > Internet

> # Evaluating ElastiCache

- > In-memory Database
- > 2 Engines you can use:
   - > Redis
   - > Memcached
- > Low latency in response times
- > Enables scaling and replicas to meet application demand
- > Handles common use cases such as;
   - > Database layer caching
   - > Session storage

## App Integration Services

> ### Amazon Simple Notification Service (SNS)

- > Fully managed publication / subscription messaging service
- > Enables you to create decoupled applications
- > Organised according to topics
- > Integrates with multiple AWS Services
- > Provides end user notifications across SMS, email and push notifications.

> ### Amazon Simple Queue Service (SQS)

- > Fully managed message queue service
- > Enables you to create decoupled and fault tolerance apps
- > Supports up to 256KB data payload
- > Allows messages to be stored up to 14 days
- > Provides 2 types of queues;
   - > Standard queue
   - > First in First out queue (FIFO)

> ### AWS Step Functions

- > Enables orchestration of workflows through a fully managed service
- > Supports serverless architectures
- > Can support complex workflows including error handling
- > Charged per state transition along with the other AWS services leveraged

# Negotiating Networking

> ### Cloud Networks

- > Amazon VPC
   - > Define and provision an isolated network for your AWS  resources
- > AWS Transit Gateway
   - > Connect VPCs and on-premise networks
- > AWS Privatelink
   - > Provide private connectivity between VPCs and on-prem applications
- > Amazon Route 53
   - > Host your own managed DNS

> ### Network Scaling

- > Elastic Load Balancing
   - > Automatically distribute network traffic across a pool of resources
- > AWS Global Accelerator
   - > Direct traffic through the AWS global network to improve global application performance

> ### Content Delivery

- > Amazon CloudFront
   - > Securely deliver data, videos and applications to customers globally with low latency and high transfer speeds

> # Valuing VPC (Virtual Private Cloud)

- > Lets you create a private network on AWS

> # Choosing CloudFront

- > Increases security
- > Traffic spike protection
- > data is cached and delivered from Edge locations (closest point to the users location)
- > Lamba@Edge
- > Real-time metrics
- > Cost Effective

> # Revising Route 53

- > Simple Routing policy
- > Weighted policy (evenly spread IP addressed to duplicate websites,)
- > Geo Policy
- > Latency policy
- > Failover policy
- > Multivalue answer policy

# Memorising Management and Governance

> ## Account Management Services

> #### AWS Control Tower

- > Set up and govern a source multi-account AWS environment
- > Centralises users across all AWS accounts
- > Provides a way to create new AWS accounts based on templates
- > Integrates Guardrails for accounts
- > Includes a dashboard to gain operational insights for a single pain view

> #### AWS Organisations

- > Centrally manage and govern your environments across multiple AWS accounts

> #### AWS Budgets

- > Improve your planning and cost control

> ## Provisioning Services

> #### AWS CloudFormation

- > Model and provision your resources via code
- > Provision infrastructure based on templates
- > No additional charge
- > Templates can be YAML or JSON
- > Enables IAC
- > Manages dependancies between resources
- > Provides drift detection to find changes in your infrastructure

> #### AWS Service Catalogue

- > Organise and govern your own curated catalog of AWS products

> #### AWS OpsWorks

- > Provides managed instances of Chef and Puppet
- > Config is defined as code for servers
- > Chef and Puppet manage the lifecycle of those config changes with the servers
- > Works in hybrid cloud architecture for both cloud-based and On-Prem

![Image.jpeg](https://res.craft.do/user/full/f14daadb-9175-da55-3d5f-ffa67ffaaf79/doc/39DEEE3C-3DCF-4E4B-82E5-A0EF8F15B9F9/BDD4A771-8C8E-47E5-8189-19C2F38A513F_2/PBIsWI6wu1FufeU1zA7iDZkNy2vdIYCGZjtoC12n9SIz/Image.jpeg)

> #### AWS Marketplace

- > Find, test, buy and deploy software that runs on AWS

> ## Operation Services

> #### Amazon CloudWatch

- > Observe your services via metrics and logging
- > Monitoring and management system
- > Enables alarms based on metrics
- > Visualisation capabilities for metrics

> #### AWS Config

- > Record and evaluate configs of AWS resources
- > Config history for infrastructure
- > Works against rules that you can customise or even create custom validations
- > Includes conformance packs for compliance standards including PCI-DSS
- > Can work with AWS Organisations for both cross regions and cross account set up
- > Provides remediation steps for infrastructure not meeting criteria

> ### AWS CloudTrail

- > Track all user activity across your AWS accounts
- > Inserts audit trail in an S3 bucket or into CloudWatch logs
- > Logs events in regions in which they occur
- > Meets many compliance requirements for infrastructure auditing
- > As a best practice, it should be enabled on every AWS account
- > Can be consolidated into an Organisational trail using AWS Organisations

> #### AWS Systems Manager

- > Optimise performance and security while managing a large amount of systems
- > Enables automation tasks for common maintenance actions
- > Gives a secure way to access servers using only AWS credentials
- > Stores commonly used parameters securely for operational use

> #### Amazon X-ray

- > Analyse and debug production applications

### Managing Infrastructure

![Image.jpeg](https://res.craft.do/user/full/f14daadb-9175-da55-3d5f-ffa67ffaaf79/doc/39DEEE3C-3DCF-4E4B-82E5-A0EF8F15B9F9/6F000229-7233-4A07-ADA0-6DE377294305_2/kX7Oz9RHX3I9PzSii01CuvtwBGEGJdSMyQRkeAsDgY4z/Image.jpeg)

> ## Composing CloudFormation

- > JSON & YAML languages can be used
- > Set up your cloud infrastructure through code
- > Use 'Git' to keep track of version controls
- > Automation

> ## Amazon CloudWatch

- > Collect metrics from services
- > Integrates with 70+ AWS Services
- > Lots of predefined metrics
- > Log Storage - Search and analyse
- > Example:
   - > SSH Login > EC2 instance > CloudWatch Logs > CloudWatch Filter > CloudWatch Alarm (You can use cloud watch to log failed SSH logins over a 5 min period and notify you)

> ## Applying AutoScaling

- > Scale your instance capacity automatically according to your needs
- > Auto Scaling Group
- > Load Balancer distributes the connections to the servers as they appear and disappear as required
- > High availability
- > Better fault tolerance
- > Better cost management
- > EC2, DynamoDB, Aurora

> ## Machine Learning AI

- > Amazon Kendra
   - > Intelligent Search
- > Amazon Personalise
   - > Personalised recommendations

> ## Machine Learning Business Metrics

- > Amazon Lookout for Metrics
   - > Detect unexpected changes; eg revenue performance and customer retention and identify root causes
- > Amazon Forecast
   - > Build accurate forecasting models
- > Amazon Fraud Detector
   - > Identify potentially fraudulent online activities

> ## Machine Learning Vision

- > Amazon Rekognition
   - > Analyse images and videos and extract meaning

> ## Machine Learning Language Services

- > Amazon Polly
   - > Turn text into life-like speech
- > Amazon Transcribe
   - > Add high quality speech to text capabilities to your applications
- > Amazon Lex
   - > Easily build conversational agents or chat bots

> ## Recognising Recognition

- > Analyse images and videos and extract meaning
- > Image Moderation
- > Facial recognition
- > PPE recognition
- > Celebrity recognition

> ## AWS DeepRacer

- > Reinforcement training

> ## Comparing CodeGuru

- > Usually code goes through Code Review
- > Uses machine learning to review code
- > Detect critical issues
- > Find security vulnerabilities
- > Point out hard-to-find bugs
- > CodeGuru Profiler
   - > Analyses code to find 'expensive' code (CPU usage)
   - > Understand run time of your applications
- > CodeGuru Reviewer
   - > service that uses program analysis and machine learning to detect potential defects that are difficult for developers to find and offers suggestions for improving your Java and Python code.
   - > By proactively detecting code defects, CodeGuru Reviewer can provide guidelines for addressing them and implementing best practices to improve the overall quality and maintainability of your code base during the code review stage.

