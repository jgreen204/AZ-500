# Intro to Security and Architecture on AWS

## AWS Architecture Core Concepts

> ### Shared Responsibility Model

![Image.jpeg](https://res.craft.do/user/full/f14daadb-9175-da55-3d5f-ffa67ffaaf79/doc/AFCBEB1F-427A-481E-A270-BFE648551D97/AEE4E035-29DC-483F-8779-16FEB5F2E8F2_2/b09bpAuymiyMVgpzOPYQIhOGMAq0uB8u31NZpLu170Yz/Image.jpeg)

> ### AWS Well-Architected Framework

![Image.jpeg](https://res.craft.do/user/full/f14daadb-9175-da55-3d5f-ffa67ffaaf79/doc/AFCBEB1F-427A-481E-A270-BFE648551D97/24EDFFF6-8314-40B3-9AD3-B7FE36D47A18_2/wbzJ7wViUfeTmUkpgBGx1p8vhkiLzu5dJtE8YBpa2vIz/Image.jpeg)

> ### Pillars of a well-architected Framework

![Image.jpeg](https://res.craft.do/user/full/f14daadb-9175-da55-3d5f-ffa67ffaaf79/doc/AFCBEB1F-427A-481E-A270-BFE648551D97/BCCF052E-973E-4930-B874-B45FD301499A_2/7kVsiZZqxgC6xvcaQVdYrHHCJoz2yrSiLeufi1yx7S8z/Image.jpeg)

> ### High Availability and Fault Tolerance

#### Reliability on AWS

- > Fault Tolerance
   - > Being able to support the failure of components within your architecture
- > High Availability
   - > Keeping your entire solution running in the expected manner despite issues that may occur.

### Building Solutions on AWS

- > Most managed AWS services provide High-availability out of the box
- > When building solutions directly on EC2, fault tolerance must be architected
- > Multiple availability zones should be leveraged
- > Some services can enable fault tolerance in your custom apps
   - > Simple Queue Service (SQS)
   - > Route 53

> ### Compliance

- > PCI-DSS
   - > Compliance standard for processing credit cards
- > HIPPA
   - > Compliance standard for health care data (US)
- > SOC1, SOC2 & SOC3
   - > Third party reviews of operational processes
- > FedRAMP
   - > Standards for U.S government data handling
- > ISO 27018
   - > Standard for handling Personal Identifiable Info (PII)

> ### Acceptable Use Poilcy

![Image.jpeg](https://res.craft.do/user/full/f14daadb-9175-da55-3d5f-ffa67ffaaf79/doc/AFCBEB1F-427A-481E-A270-BFE648551D97/979BCFC1-46B5-4054-8771-B3D0EE258640_2/vP8toa7OzfNvyCyBmbdIVwwHN0K2nnkNj397wkwdso0z/Image.jpeg)

# AWS Identities and User Management

> ### Introduction into AWS IAM

- > Service that controls access to AWS resources
- > Using the service is free
- > Manages both authentication and authorisation
- > Supports identity federation through SAML providers including AD

#### AWS IAM Identities

- > User
   - > Account for a single individual to access AWS resources
- > Groups
   - > Allows you to manage permissions for a group of IAM users
- > Roles
   - > Enables a user or AWS service to assume permissions for a task

#### Policies in AWS IAM

- > A JSON document that defines permissions for an AWS IAM identity (principal)
- > Defines both the AWS service that the identity can access and what actions can be taken on that service.
- > Can be either customer managed or managed by AWS

#### AWS IAM Best Practices

- > MFA
   - > Physical or virtual device that generates a token for login
- > Least Privilege Access
   - > users should only be granted access to AWS resources that are required for their current tasks

> ### Amazon Cognito

- > Fully managed User directory service for custom apps
- > Provides UI components for many platforms
- > Provides security capabilities to control account access
- > Enables controlled access to AWS resources
- > Can work with social and enterprise identity providers
   - > Google
   - > Amazon
   - > Facebook
   - > AD
   - > SAML 2.0 providers

# Data Architecture in AWS

> ### Integrating On-Premise Data

- > #### AWS Storage Gateway
   - > Hybrid-Cloud Storage Service
   - > Integrates cloud storage into your local network
   - > Deployed as a VM or specific hardware appliance
   - > Integrates with S3 and EBS
   - > Supports three different gateway types:
      - > #### Tape Gateway
         - > Enables tape backup processes to store data in the cloud on virtual tapes.
      - > #### Volume Gateway
         - > Provides cloud based iSCSI volumes to local apps
      - > #### File Gateway
         - > Stores files in Amazon S3 while providing cached low-latency access.
- > #### AWS DataSync
   - > Automated data transfer service
   - > Leverages the DataSync agent deployed as a VM on your network
   - > Integrates with S3, EFS and FSx for Windows File Server on AWS
   - > Greatly improved speed of transfer due to custom protocol and optimisation
   - > Charged per GB data transferred

> ## Processing Data

> ### Data Processing Services

- > #### AWS Glue
   - > Managed Extract, Transform, and load (ETL) Service
   - > Fully managed ETL service on AWS
   - > Supports data in Amazon RDS, DynamoDB, Redshift and S3
   - > Supports a serverless model of execution
- > #### AWS EMR
   - > Big-Data cloud processing using popular tools
   - > Enables big data processing on Amazon EC2 and S3
   - > Supports popular open-source frameworks and tools
   - > Operates in a clustered environment without additional configuration
   - > Supports many big data use cases
- > #### Supported Amazon EMR Frameworks
   - > Apache Spark
   - > Apache Hive
   - > Apache HBase
   - > Apache Flink
   - > Apache Hudi
   - > Presto
- > #### AWS Data Pipeline
   - > Data workflow orchestration service across AWS Services
   - > Managed ETL (extract, transform and load) service on AWS
   - > Manages data workflow through AWS Services
   - > Supports S3, EMR, Redshift, DynamoDB and RDS

> ## Analysing Data

- > #### Amazon Athena
   - > Service that enables querying of data stored in Amazon S3
   - > Fully managed serverless service
   - > Enables querying of large-scale data stored within Amazon S3
   - > Queries are written using standard SQL
   - > Charged based on data scanned for query
- > #### Amazon Quicksight
   - > Business intelligence service enabling data dashboards
   - > Fully managed BI service
   - > Enables dynamic data dashboard based on data stored in AWS
   - > Charged on per-user and per-session pricing model
   - > Multiple version provided based on needs
- > #### Amazon CloudSearch
   - > Managed search service for custom apps
   - > Fully managed search service on AWS
   - > Supports scaling of search infrastructure to meet demand
   - > Charged per hour and instance type of search infrastructure
   - > Enables developers to integrate search into custom applications

> ## Integrating AI and Machine Learning

- > #### Amazon Rekognition
   - > Computer vision service powered by ML
   - > Fully managed image and video recognition deep learning service
   - > Identifies objects in images
   - > Identifies objects and action in videos
   - > Can detect specific people using facial analysis
   - > Supports custom labels for your business objects
- > #### Amazon Translate
   - > Text translation service powered by ML
   - > Fully managed service for translation of text
   - > Currently supports 54 languages
   - > Can perform language identification
   - > Works both in batch and real-time
- > #### Amazon Transcribe
   - > Speech to text solution using ML
   - > Fully managed speech recognition service
   - > Recorded speech is converted into text in custom apps
   - > Included a specific sub-service for medical use
   - > Supports batch and real-time transcription
   - > Currently supports 31 languages

# Disaster Recovery on AWS

> ## Disaster Recovery Architectures

> #### Disaster Recovery Scenarios

![Image.jpeg](https://res.craft.do/user/full/f14daadb-9175-da55-3d5f-ffa67ffaaf79/doc/AFCBEB1F-427A-481E-A270-BFE648551D97/31EF33F8-8E5B-4912-842D-911746CEB428_2/8D3IIrntiZhi26nxYGYcGaz6W3eL5aKlGQljfuX9j5Qz/Image.jpeg)

> #### Backup and Restore

- > Production data is backed up into Amazon S3.
- > Data can be stored in either standard or archival storage classes.
- > EBS data can be stored as snapshots in Amazon S3 also
- > In a Disaster Recovery event, a process is started to launch new environment.
- > This approach has the longest recovery time.
- > Least cost!!

> #### Pilot Light

- > Key infra components are kept running in the cloud
- > Designed to reduce recovery time over the Backup and Restore approach
- > Does incur cost of this infra continually running in the cloud
- > AMI's are prepared for additional systems and can be launched quickly

> #### Warm Standby

- > A scaled-down version of the full environment is running in the cloud
- > Critical systems can be running on less capable instance types
- > Instance types and other systems can be rammed up for disaster recovery event
- > Does incur cost of this infra continually running in the cloud

> #### Multi Site

- > Full environment is running in the cloud at all times
- > Utilises instance types needed for production not just recovery
- > Provides a near seamless recovery process
- > Incurs the most cost over the other approaches

> ## Selecting a Disaster Recovery Architecture

> #### Recovery Time Objective (RTO)

- > The tim,e it takes to get your systems back up and running to the ideal business state after a disaster recovery event.

> #### Recovery Point Objective (RPO)

- > The amount of data loss (in terms of time) for a production system during a disaster recovery event.

# Architecting Applications on Amazon EC2

> ## Scaling EC2 Infrastructure

> #### EC2 Horizontal Scaling Services

- > #### Auto-scaling Group
   - > Set of EC2 instances with riles for scaling and management
   - > Launch template defines the instance config for the group
   - > Defines the min, max and desires number of instances
   - > Performs health checks on each instance
   - > Exists within 1 or more availability zones in a single region
   - > Works with on-demand and spot instances
- > Elastic Load Balancer
   - > Distributes traffic across multiple targets

> #### AWS Secrets Manager

- > Secure way to integrate credentials, API keys, tokens and other secret content
- > Integrates natively with RDS, DocumentDB and RedShift
- > Can auto-rotate credentials with integrated services
- > Enables fine-grained access control to secrets

> ## Controlling Access to EC2 Instances

> ### Security in Amazon VPC

> #### Security Groups

- > Serves as a firewall for your EC2 instances
- > Control inbound and outbound traffic
- > Works at the instance level
- > EC2 instances can belong to multiple security groups
- > VPC's have default security groups
- > Must be explicitly associated with an EC2 instance
- > By default all outbound traffic is allowed

> #### Network ACL's

- > Works at the subnet level with an VPC
- > Enables you to all and deny traffic
- > Each VPC has a default ACL that allows all inbound and outbound traffic
- > Custom ACL's deny all traffic until rules are added

> #### AWS VPN

- > Creates an encrypted tunnel into your VPC
- > Can be used to connect your data centre or even individual client machines
- > Supported in two services;
   - > Site-to-site VPN
   - > Client VPN

> ## Protecting Infrastructure from Attacks

> #### AWS Sheild

- > Managed DDoS protection service for apps on AWS
- > Enables on-going threat detection and mitigation
- > Has two different service levels;
   - > Standard
   - > Advanced

> #### Amazon Macie

- > Data protection service powered by ML
- > Analyses data stored in Amazon S3
- > It can detect personal information and intellectual property in S3
- > Provides dashboards that show how the data is being stored and accessed
- > Enables alerts if it detects anything unusual about data access

> #### Amazon Inspector

- > Automated security assessment service for EC2 instances
- > Enables scanning of Amazon EC2 instances for security vulnerabilities
- > Charged by instance per assessment run
- > Two types of rules packages;
   - > Network reachability assessment
   - > Host assessment

> ## Deploying Pre-defined Solutions

> #### AWS Service Catalogue

- > Managed catalog of IT services on AWS for an organisation
- > Targeted to serve as an organisational service catalog for the cloud
- > Can include single server image to multi-tier custom apps
- > Enables organisations to leverage services that meet compliance
- > Supports a lifecycle for services released in the catalog

> #### AWS Marketplace

- > Catalog of software to run on AWS from third-party providers
- > Curated catalog of third-party solutions for customers to run on AWS
- > Provides AMI's, CloudFormation stacks, and SaaS based solutions
- > Enables different pricing options to overcome licensing in the cloud
- > Charges appear on your AWS bill

> ## Developer Tools

> #### AWS CodeCommit

- > Managed source control service
- > Utilises Git for repos
- > Control access with IAM policies
- > Serves as an alternate to GitHub and BitBucket

> #### AWS CodeBuild

- > Fully managed build and continuous integration service on AWS
- > Don't have. to worry about maintaining infra
- > Charged per minute for compute resources you utilise

> #### AWS CodeDeploy

- > Managed deployment service for deploying your custom apps
- > Deploys to Amazon EC2, AWS Fargate, AWS Lambda and On-Prem servers
- > Provides dashboards for deployments in the AWS console

> #### AWS CodePipeline

- > Fully managed continuous delivery service on AWS
- > Provides the capabilities to automate building, testing and deploying
- > Integrates with other developer tools like GitHub

> #### AWS CodeStar

- > Workflow tool that automates the use of the other developer services
- > Creates a complete continuous delivery toolchain for a custom application
- > Provides custom dashboards and configs in the AWS console

