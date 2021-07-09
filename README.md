# Create-Webserver-in-AWS
Webserver can be seen in action even without log-in to your EC2 instance by providing bootstrap script in to user data section of EC2.

#!/bin/sh
sudo yum update -y
sudo yum install httpd -y
sudo service httpd start 
chkconfig httpd on 
cd /var/www/html
cat >> index.html << EOF
<html><body> this is first ec2 instance in az-a </body></html>
EOF
