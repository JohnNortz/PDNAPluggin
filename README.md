# PDNAPluggin

to load this stack into your AWS account follow the following link: https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=PDNAMonitorPlusMailer&templateURL=https://s3-us-west-2.amazonaws.com/allyislambdafunctionsbucket/PDNAMonitorPlusMailer.template

Instructions: 
1)	Click [Button] to download the template and be navigated to your AWS accounts CloudFormation page. 
2)	On the first fill out the following fields:  
To find your personal PDNA key visit: https://testpdnaui.azurewebsites.net/ 
For Sender Email field, the email must be verified by your AWS account, visit https://us-west-2.console.aws.amazon.com/ses/home?region=us-west-2#verified-senders-email 
3)	On Options page, click Next
4)	On Review, acknowledge the terms and click ‘Create,’ your stack will then be created.
5)	Once the stack has finished, navigate to your Amazon S3 management page https://s3.console.aws.amazon.com/s3 and select any bucket you want monitored by PDNA
6)	From the bucket landing page, Select Properties, then Events 
7)	On the events page, fill in the following fields:  
Select a name for your event, Select ObjectCreate, Select Lambda Function under the Send To dropdown, and finally select the lambda function created by the stack.
8)	Select Save
Your bucket is now ready to be monitored by PDNA, repeat steps 6-8 for each bucket you want monitored by PDNAs services. 
