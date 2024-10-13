AWS Cloud Cost Optimization - Identifying Stale Resources
-------------------------------------------------------

Created a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

Description:
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

Created EC2 instance and Snapshot: 
![image](https://github.com/user-attachments/assets/0075c297-129f-4dad-921d-a4dfeadcc27c)

Deleted the EC2 instance:
![image](https://github.com/user-attachments/assets/1630a983-5dea-482c-8e4e-8cbed5912352)

Execution: 
![image](https://github.com/user-attachments/assets/a5159e91-4f1e-45ca-8d82-eda6d7982969)

Lambda function identified EBS snapshots that are no longer associated with any active EC2 instance and deleted:
![image](https://github.com/user-attachments/assets/2346b680-6be4-4424-b24d-af3420682862)
