# AWS Security

- [AWS Security](#aws-security)
  - [Introduction](#introduction)
  - [Documentation](#documentation)
  - [Domains](#domains)
    - [Incident Response](#incident-response)
    - [Logging and Monitoring](#logging-and-monitoring)
    - [Infrastructure Security](#infrastructure-security)
    - [Indetity and Access Management](#indetity-and-access-management)
    - [Data Protection](#data-protection)

## Introduction

## Documentation

- [AWS Certified Security Specialty](https://aws.amazon.com/certification/certified-security-specialty/)

## Domains

AWS Certified Security specialty is divided into the following 5 domains:
1. Incident Response
2. Logging and Monitoring
3. Infrastructure Security
4. Identity and Access Management
5. Data Protection

The following section briefly summarizes the blueprint requirements and related AWS services for each domain.

### Incident Response

Blueprint requirements:
- Given an AWS abuse notice, evaluate the suspected compromised instance or exposed access keys
- Verify that the Incident Response plan includes relevant AWS services
- Evaluate the configuration of automated alerting and execute possible remediation of security-related incidents and emerging issues

Related AWS Services:
- **AWS Config** -  Create AWS Config rules that automatically take action in response to change in your environment, for example remove offending EC2 Security Group rule, isolate a resource upon intrusion detection or restore configuration to a baseline.
- **AWS Lambda** - Use serverless compute service to run code without provisioning or managing servers. Lambda can use Triggers to execute upon specific events or incidents.
- **Amazon Detective** - Collects log data from AWS resources and than uses Machine Learning, Statistical analysis and graph theory to build linked set of data.
- **CloudEndure Disaster Recovery** - Provides DR services for applications hosted in AWS or on-prem. 

### Logging and Monitoring

Blueprint requirements:
- Design and implement security monitoring and alerting
- Troubleshoot security monitoring and alerting
- Design and implement a logging solution
- Troubleshoot logging solutions

Related AWS Services:
- **AWS CloudWatch** - Collects metrics form resources, monitors log files, sets alarms and can automatically react to changes
- **AWS CloudTrail** - Tracks user activity and API usage to enable governance, compliance and operational auditing
- **AWS Config** - Records and evaluates configurations of resources to enable compliance auditing, resource change tracking and security analysis
- **VPC Flow Logs** - Captures information about network traffic within VPC. Records are stored using AWS CloudWatch Logs
- **Amazon Security Hub** - Provides central view or single pane of glass for security alerts and can automate compliance checks
- **Amazon GuardDuty** - Provides threat detection and monitoring to protect AWS accounts and workloads
- **Amazon Inspector** - Automates security assessments to help imprve security and compliance of applications deployed on AWS

### Infrastructure Security

Blueprint requirements:
- Design edge security on AWS
- Design and implement a secure network infrastructure
- Troubleshoot a secure network infrastucture
- Design and implement host-based security

Related AWS Services:
- **AWS VPC** - Provides a logically isolated section of AWS where you can launch resources
- **AWS Privatelink** - Provides private connectivity between VPC and AWS services or on-prem networks without exposing traffic over Internet
- **AWS Shield** - Provides a manage Distributed Denial of Service (DDoS) protection
- **AWS WAF** - Protects web applications from common application exploits
- **AWS Firewall Manager** - Provides central view or single pane of glass for managing AWS WAF rules across accounts and applications
- **AWS Systems Manager** - Configuration management services that can manage cloud or on-prem instances (OS Configuration and Patching, Image creation)

- [VPC Security Groups](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html)
- [VPC Network ACLs](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html)

### Indetity and Access Management

Blueprint requirements:
- Design and implement a scalable authorization and authentication system to access AWS resources
- Troubleshoot an authorization and authentication system to access AWS resources

Related AWS Services
- **AWS Identity and Access Management (IAM)** - Manages identities and permissions for accessing AWS services and resources
- **AWS Organizations** - Policy-based management for multiple AWS accounts
- **AWS Single Sign-on (SSO)** - Centrally manage SSO access to multiple AWS accounts and business applications
- **AWS Directory Services** - Provides managed Microsoft Active Directory
- **AWS Resource Access Manager** - Provides simple, secure service to share AWS resources
- **Amazon Cognito** - Provides user sign-up, sign-in, and access control to your web or mobile applications

Resources:
- [IAM Policy evaluation logic](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html)
- [IAM JSON policy elements reference](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements.html)


### Data Protection

Blueprint requirements:
- Design and implement key management and use
- Troubleshoot key management
- Design and implement a data encryption solution for data at rest and data in transit

Related AWS Services
- **AWS Key Management Service (KMS)** - Creates and manages keys used to encrypt data
- **Server-Side Encryption** - Flexible data encryption using AWS service managed keys
- **AWS Secrets Manager** - Creates and manages credentials (databasem, API keys) and secrets
- **AWS CloudHSM** - Managed hardware security module (HSM)
- **AWS Certificate Manager** - Creates, manages and deploys SSL/TLS certificates
- **AWS VPN** - Provides network extension using encrypted tunnel over untrusted network
- **AWS Macie** - Discovers and protects sensitive data at scale using machine learning 