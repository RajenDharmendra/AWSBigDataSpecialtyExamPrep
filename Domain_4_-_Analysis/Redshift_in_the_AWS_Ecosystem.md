### Redshift in the AWS Ecosystem

* S3 will probably be the main source for loading and unloading data, all done in parallel

* Can use **copy** command to load data into Redshift tables from S3 and DynamoDB (also [EMR](http://docs.aws.amazon.com/redshift/latest/dg/loading-data-from-emr.html) and EC2 instances

copy thermostat_logs from ‘s3://mybucket/my_key/blah/myfile.csv’ credentials ‘aws_iam_role=arn:aws:iam::account_id:role/’

Read: 

copy table_name from s3_location credentials role_name

NOTE - using an IAM role here instead of a username/password or secret keys

* Can use SSH to copy data into Redshift from EMR or EC2 instance

* Can use AWS **Data Pipeline** to schedule & execute data flows to Redshift, or just use it to copy data in without scheduling.  Can also load to RDS or unload from Redhsift.

* **Lambda** - drop files in S3 and automatically have them pulled into Redshift, or manage snapshots via Lambda

* **QuickSight** - BI tool for Redshift

* **AWS Database Migration Service** - migrate data from on-prem or AWS databases to Redshift

* **Kinesis Streams, Firehose & Analytics**

    * **Streams** - streaming data to Redshift

    * **Firehose** - if you don’t need a custom application

    * **Analytics** - use SQL to analyze data from Firehose → Redhsift

* **Amazon Machine Learning** - Can dump data from Redshift into S3 and use Amazon ML to do predictive analytics on it

---
* [Back: Redshift Architecture (10:23)](Redshift_Architecture.md)
* [Next: Columnar Databases (5:16)](Redshift_Columnar_Databases.md)
