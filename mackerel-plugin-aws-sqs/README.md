mackerel-plugin-aws-sqs
=================================

AWS SQS custom metrics plugin for mackerel.io agent.

## Synopsis

```shell
mackerel-plugin-aws-sqs -endpoint=<SES Endpoint URL> [-access-key-id=<id>] [-secret-access-key=<key>] [-tempfile=<tempfile>]
```
* if you run on an ec2-instance and the instance is associated with an appropriate IAM Role, you probably don't have to specify `-access-key-id` & `-secret-access-key`

## AWS Policy
the credential provided manually or fetched automatically by IAM Role should have the policy that includes actions, 'sqs:GetSendQuota' and 'sqs:GetSendStatistics'

## Example of mackerel-agent.conf
```
[plugin.metrics.aws-sqs]
command = "/path/to/mackerel-plugin-aws-sqs -endpoint=https://email.us-west-2.amazonaws.com"
```
