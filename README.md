# **aws-cloud-cost-optimizer-lambda**
# Identifying Stale EBS Snapshots
In this example, we will create a Lambda function to identify EBS snapshots that are no longer associated with any active EC2 instance and delete them to save on storage costs.

# Description:
The Lambda function retrieves all EBS snapshots owned by the account ("self") and also gets a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if it exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

![process](https://github.com/user-attachments/assets/639f4e43-c3d8-4e96-8697-174c19ff1660)


# Introduction to AWS Lambda Serverless Computing

# What is Serverless Computing?
Serverless computing does not imply the absence of servers; rather, it refers to a cloud computing model where developers do not need to manage servers directly. This allows developers to concentrate on writing and deploying their code while the cloud provider handles the infrastructure.
# Understanding AWS Lambda
AWS Lambda is a standout service in the serverless ecosystem. It is a compute service that enables users to execute code in response to events without the need for server provisioning or management. Lambda automatically scales applications according to incoming requests, alleviating concerns about capacity planning and server upkeep.
# Key Features of AWS Lambda

Event-Driven Execution: AWS Lambda functions are triggered by events, such as data changes or user requests..

Automatic Scaling: The service adjusts resources based on demand, ensuring high availability without manual intervention.

Zero Server Management: Users can focus solely on coding, as AWS manages all underlying infrastructure.

Cost Efficiency: Billing is based on actual usage; users pay only for the compute time consumed during code execution.

# Common Use Cases

AWS Lambda is particularly effective for various applications, including:

Data Processing: Automatically process data from sources like Amazon S3.

Real-Time Analytics: Handle streaming data for immediate insights.

Business Process Automation: Streamline operations by automating repetitive tasks.

# Advantages and Disadvantages
# Advantages:

Scalability: Applications can seamlessly scale up or down based on workload.



Cost Savings: Users incur costs only when their code runs, making it economical for sporadic workloads.

# Disadvantages:

Cold Start Latency: There may be delays when functions are invoked after a period of inactivity, affecting performance.


# RESULTS: 

![stale_snapshot](https://github.com/user-attachments/assets/168a54f5-ad9a-4ac8-a528-9bc4f7a2d401)

![snapshot_deleted](https://github.com/user-attachments/assets/997ef366-3560-496e-8e48-ebd60f53b391)



