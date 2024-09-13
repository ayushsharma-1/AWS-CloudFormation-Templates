# AWS-CloudFormation-Templates
 This repository offers AWS CloudFormation templates to automate the provisioning and management of AWS infrastructure. Using Infrastructure as Code (IaC), these templates enable efficient, scalable cloud automation. Each template is modular, allowing customization and reuse to fit specific automation needs across AWS services.

## Overview

This repository provides a collection of AWS CloudFormation templates aimed at automating the deployment and management of AWS services. By leveraging Infrastructure as Code (IaC), these templates help to standardize, speed up, and secure the provisioning of AWS resources, making cloud management more efficient and reliable.

The templates are designed to cover a wide range of AWS services and scenarios, including:
- Virtual Private Cloud (VPC) setup
- EC2 instance provisioning
- Load balancer configurations
- Auto-scaling group setups
- S3 bucket policies and lifecycle configurations
- RDS (Relational Database Service) instance setup
- Lambda function deployment
- Security group configurations
- CloudWatch monitoring and alarms

## Features

- **Automation**: Simplifies the process of deploying complex AWS resources.
- **Modularity**: Templates are modular and reusable, allowing you to adapt them to specific use cases.
- **Scalability**: Supports the automation of scalable architectures to handle varying levels of demand.
- **Cost-Effectiveness**: Optimized templates to reduce costs by using the right services and configurations.

## Prerequisites

To use the CloudFormation templates, you will need:
- An AWS account
- AWS CLI installed and configured on your machine
- Permissions to create resources in AWS using CloudFormation
- Familiarity with CloudFormation syntax (YAML or JSON)

## How to Use

1. Clone the repository:
    ```bash
    git clone https://github.com/ayushsharma-1/AWS-CloudFormation-Templates.git
    cd AWS-CloudFormation-Templates
    ```

2. Select the CloudFormation template you need for your automation task from the `/templates` directory.

3. Deploy the template using AWS CLI:
    ```bash
    aws cloudformation create-stack --stack-name <stack-name> --template-body file://<template-file>.yaml --parameters ParameterKey=<Key>,ParameterValue=<Value>
    ```

4. Monitor the deployment status using:
    ```bash
    aws cloudformation describe-stacks --stack-name <stack-name>
    ```

5. Once deployed, AWS will provision the resources as specified in the template.

## Template Structure

- `/templates/`: Contains all the CloudFormation templates categorized by AWS services.
- `/examples/`: Contains sample configurations that demonstrate how to use the templates.
- `/docs/`: Contains detailed documentation on each template and its use cases.

## Example Usage

To deploy an EC2 instance with a VPC and a security group:
1. Navigate to the EC2 template in the `/templates/ec2` folder.
2. Customize the parameters in the YAML file as needed.
3. Deploy the template using the AWS CLI.

```bash
aws cloudformation create-stack --stack-name ec2-instance-stack --template-body file://ec2-instance.yaml --parameters ParameterKey=InstanceType,ParameterValue=t2.micro ParameterKey=KeyName,ParameterValue=MyKeyPair

### Contributing
Contributions are welcome! Please follow the steps below:

1. Fork the repository.
2. Create a new branch:  
   `git checkout -b feature/my-feature`
3. Commit your changes:  
   `git commit -m 'Add some feature'`
4. Push to the branch:  
   `git push origin feature/my-feature`
5. Open a pull request.

### License
This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

### Support
For issues or feature requests, please create a GitHub issue in the repository or reach out via email at ayushsharma18001@gmail.com.

