## Developing Messaging Solutions with Amazon SNS and Amazon SQS

![AWS SQS & SNS Lab](/lab-5-sqs-sns/images/lab-5-sqs-sns.png)

### Develop an application with AWS SNS and SQS services
- Send emails to customers about their orders.
- Send order message to multiple amazon sqs queues so, message can be processed by another applications.
- Recieve and process messages from amazon sqs queues.

### Lab steps with java code
1. We will setup Amazon SNS topics and SQS queues.
    - EmailSNSTopic: Amazon SNS topic to send email notifications
    - OrderSNSTopic: Amazon SNS topic to send order message to subscribers
    - MySQSQueue_A: SQS queue processed by SQSConsumer class
    - MySQSQueue_B: SQS queue processed by other applications

2. In AWS console go to SNS and select Get started on the main page.
3. Create new topic with below details
    - Type: Standard
    - Name: EmailSNSTopic
    - Display name: EmailTopic

4. In the Topic page note down the ARN of EmailSNSTopic topic into a notepad for further use.
5. In the Topic detail page for EmailSNSTopic navigate down to Subscriptions tab and select Create subscription
6. Create subscription with below details
    - Topic Arn: Enter the arn of EmailSNSTopic.
    - Protocol: Email
    - Endpoint: Enter your email address for subcription
    - Choose Create subsctiption


