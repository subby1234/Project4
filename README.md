# Project4

Follow the below mentioned steps - 

1.Subscribe for the Topic created in SNS service by CF template.
2.Create a role for EC2 with access of SNS.
3.Create an VPC interface endpoint for SNS service.

Connect to your EC2 and check the internet connectivity by pinging google.com [PING google.com] you will see that you are not able ping it because we have restricted the connection with the VPC only.

Then Run this command to send the message to SNS Topic:

-> aws sns publish --region /*your aws region*/ --topic-arn /* arn of your sns-topic*/ --message /*your message that you want send*/

Ex :- aws sns publish --region us-east-2 --topic-arn arn:aws:sns:us-east-2:124058707612:VPCE-Tutorial-Topic --message "this is my project3"
