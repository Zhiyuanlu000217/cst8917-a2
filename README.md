# cst8917-a2

In the following report, I will organize the report based on each service.

# 1. Azure Functions

Overview: Azure Functions is a serverless compute service that runs event-triggered code without managing infrastructure. It offers a range of hosting plans to balance cost and performance and has strong integration with the Microsoft ecosystem.

| Category | Azure Functions | AWS Lambda | Google Cloud Functions |
| :--- | :--- | :--- | :--- |
| Core Features | Supports multiple languages. Extensive bindings/triggers for Azure services. | Broad language support. Triggers from over 200 AWS services. | Supports popular languages. Triggers for GCP services and HTTP. |
| Integration| Seamless with Azure services (Service Bus, Event Grid). Visual Studio/VS Code tooling. | Deep integration with AWS services (S3, DynamoDB). Uses SAM and CloudFormation. | Strong with GCP services. Uses Cloud Build for CI/CD. |
| Monitoring | Azure Monitor, Application Insights. Provides logs, metrics, and tracing. | Amazon CloudWatch. Offers detailed metrics, logs, and alarms. | Cloud Monitoring/Logging. Unified view of logs and metrics. |
| Pricing | Consumption Plan: Pay-per-execution ($0.20 per million) and resource consumption (GB-seconds, ~$0.000016 per GB-s). Includes a generous free grant per month. | Pay-per-request ($0.20 per million) and execution duration (GB-seconds, ~$0.00001667 per GB-s). Free tier includes 1 million requests and 400,000 GB-s. | Pay-per-invocation ($0.40 per million) and compute time (GB-seconds, CPU-seconds). Free tier includes 2 million invocations and 400,000 GB-s. |
| Strengths | - Flexible hosting plans. <br>- Excellent C#/.NET developer experience. | - Most mature and extensive ecosystem. <br>- Highly reliable. | - Fast cold starts. <br>- Competitive pricing. |
| Weaknesses | - Potential cold starts on Consumption plan. | - Can become complex in large-scale setups. | - Smaller ecosystem compared to AWS and Azure. |

