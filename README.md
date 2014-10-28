zabbix_rds_template
===================

AWS RDS Template for Zabbix

1. place the script "rds_stats.py" at zabbix-server externalscripts folder (https://www.zabbix.com/documentation/2.0/manual/config/items/itemtypes/external), make sure to have execute permission on it. 
2. Import the template "zbx_RDS_template.xml".
3. enter you aws credentials in the template's macro section   {$AWS_ACCESS_KEY},  {$AWS_SECRET_KEY}   
