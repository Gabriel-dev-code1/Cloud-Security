--Objective--

Detect IAM user creation events and trigger real-time email alerts using AWS native services.

--Services Used--

AWS IAM
AWS CloudTrail
AWS EventBridge
AWS SNS

--Architecture Flow--

IAM → CloudTrail → EventBridge → SNS → Email Alert

--Event Pattern Used--
{
  "source": ["aws.iam"],
  "detail-type": ["AWS API Call via CloudTrail"],
  "detail": {
    "eventSource": ["iam.amazonaws.com"],
    "eventName": ["CreateUser"]
  }
}

--Proof of Execution--
## 📸 CloudTrail Enabled

![CloudTrail](images/cloudtrail.png)

## 📸 Email

![EMAIL](images/email-aws.png)

## 📸 EventBridge

![EventBridge](images/eventBridge.png)

## 📸 Monitoring event
![Monitoring](images/monitoring.png)

## 📸 SNS

![SNS](images/sns.png)

## 📸 Subscription

![Subscription](images/subscription.png)


--Security Concept Demonstrated--

Real-time IAM monitoring
Event-driven architecture
Cloud-native detection engineering
Basic SOC alert simulation
