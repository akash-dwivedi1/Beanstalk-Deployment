User will access the URL which will be resolved to an endpoint from Amazon route 53. The endpoint will be of Amazon Cloudfront Content Delivery Network which will cache so many things to serve global audience. From there the request will be redirected to Application Load Balancer which is part of Elastic Beanstalk. Application LB will forward request to EC2 instance which is in an autoscaling group. Here are Tomcat application service will be running. There will be also Amazon Cloudwatch alarms which will be monitoring auto scaling groups and will scale out or scale in based on the requirement. Artifacts will be stored in s3 bucket. We can deploy latest artifact by just clicking a button. Entire frontend will be managed by Beanstalk. Backend we are using AmazonMQ as message broker service, elastic cache service and RDS.



# Prerequisites
#
- JDK 1.8 or later
- Maven 3 or later
- MySQL 5.6 or later

# Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- MySQL
# Database
Here,we used Mysql DB 
MSQL DB Installation Steps for Linux ubuntu 14.04:
- $ sudo apt-get update
- $ sudo apt-get install mysql-server

Then look for the file :
- /src/main/resources/accountsdb
- accountsdb.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < accountsdb.sql


# DevOps_Projects
