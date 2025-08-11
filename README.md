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


# 2. Azure Durable Functions

Overview: An extension of Azure Functions for writing stateful, long-running workflows. It handles orchestration, checkpointing, and state management, providing a code-first approach to complex workflows.

| Category | Azure Durable Functions | AWS Step Functions | Google Cloud Workflows |
| :--- | :--- | :--- | :--- |
| Core Features | Code-first stateful workflows. Supports patterns like Fan-out/Fan-in. | Declarative (JSON) visual workflows. Integrates with over 200 services. | Declarative (YAML/JSON) orchestration. Built for reliability. |
| Integration| Part of the Azure Functions ecosystem. Workflows are code-defined. | Integrates with Lambda, containers (ECS), and API Gateway. | Orchestrates GCP services and HTTP endpoints. |
| Monitoring | Azure Monitor. Provides detailed history and logs for each orchestration. | Console provides a visual timeline of workflow execution. | Cloud Monitoring/Logging. Provides step-by-step execution logs. |
| Pricing  | Cost is based on the underlying Azure Functions consumption. An additional cost for Durable orchestrations applies, which is not a separate line item but tied to the function's execution. | Standard Workflows: Priced per state transition ($0.025 per 1,000 transitions). Free tier includes 4,000 state transitions/month. | Pay-per-step executed. Free tier includes 5,000 steps and 2,000 external API calls per month. |
| Strengths | - Code-first approach. <br>- Strong for complex, custom logic workflows. | - Powerful visual designer. <br>- Extensive integrations across AWS. | - Simple YAML/JSON syntax. <br>- Optimized for API orchestrations. |
| Weaknesses | - Less intuitive for non-developers. | - JSON syntax can be verbose for complex flows. | - Lacks a visual designer and many pre-built connectors. |



### 3. Azure Logic Apps

Overview: A visual, low-code/no-code workflow service for automating business processes. It excels at enterprise application integration and connecting disparate systems using a large library of pre-built connectors.

| Category | Azure Logic Apps | AWS Step Functions | Google Cloud Workflows |
| :--- | :--- | :--- | :--- |
| Core Features | Visual designer, drag-and-drop interface. Hundreds of pre-built connectors. | Can use a visual Workflow Studio. Focused on orchestrating AWS services. | Code-based (YAML/JSON) service. Not a low-code/no-code tool. |
| Integration | Large library of connectors (Office 365, Salesforce, SAP). | Integrates with AWS services. Can call external APIs. | Primarily integrates with GCP services and public HTTP endpoints. |
| Monitoring | Azure Monitor. Provides run history and detailed logs in the designer. | Console visually tracks workflow executions. | Cloud Monitoring/Logging for step-by-step logs. |
| Pricing | Consumption Plan: Pay-per-action. Standard Connectors are $0.000125 per call, Enterprise are $0.001 per call. | Standard Workflows: Priced per state transition ($0.025 per 1,000 transitions). | Pay-per-step executed. Free tier includes 5,000 steps per month. |
| Strengths | - Best for non-developers and business users. <br>- Huge library of enterprise connectors. | - Versatile for both visual and code-based workflows. <br>- Powerful for orchestrating AWS services. | - Cost-effective and fast. <br>- Ideal for developer-centric orchestrations. |
| Weaknesses | - Can be more expensive for high-volume tasks. <br>- Less flexible for custom code. | - Visual designer is not as mature as Logic Apps. | - Lacks a visual designer and extensive connector library. |


