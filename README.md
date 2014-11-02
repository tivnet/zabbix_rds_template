zabbix_rds_template
===================

AWS RDS Template for Zabbix

1. place the script "rds_stats.py" at zabbix-server externalscripts folder (https://www.zabbix.com/documentation/2.0/manual/config/items/itemtypes/external), make sure it has execute permission. 
2. Import the template "rds_template.xml".
3. enter you aws credentials in the template's macro section   {$AWS_ACCESS_KEY},  {$AWS_SECRET_KEY}   
