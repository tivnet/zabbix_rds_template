zabbix_rds_template
===================

AWS RDS Template for Zabbix

1. place the script "rds_stats.py" at zabbix-server externalscripts folder (https://www.zabbix.com/documentation/2.0/manual/config/items/itemtypes/external), make sure it has execute permission (Ubuntu - /usr/share/zabbix/externalscripts). 
2. Import the template "rds_template.xml".
3. enter you aws credentials in the template's macro section ({$AWS_ACCESS_KEY},  {$AWS_SECRET_KEY}) or leave it blank to use IAM roles 
4. set you default AWS region in the template's macro section {$REGION}
5. Attach the above template to the relevant hosts. The zabbix host name must match the RDS DB Instance host name
6. note that you can override the AWS region for specific hosts by adding the {$REGION} macro to the host

Note: If you are creating a custom IAM policy, here is the json output:

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": "cloudwatch:GetMetricStatistics",
            "Resource": "*"
        }
    ]
}
```
