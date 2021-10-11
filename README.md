# aws_developer_task_2
task aim:
1.Create an AWS EC2 instance 
2.Configure the instance with Apache Webserver.
3.Download php application name "WordPress"".
4.As wordpress stores data at the backend in MySQL
5.Database server. Therefore, you need to setup a MySQL server using AWS RDS service using Free Tier.
6.Provide the endpoint/connection string to the
WordPress application to make it work. 

So here's how we can Integrating AWS RDS with WordPress Application on AWS Cloud in just 4 easy steps.

Step1: Launch an EC2 instance
To start off with the processes we first need to launch a EC2 instance as follows.

Step2: Launching a Mysql Database using RDS service

The next task is to create a Mysql Database using RDS for which we will have to follow the following steps.
Now, we need to select MySQL as our engine option, further more fill in all the details required. Here, I am using my pre-created Security Group which allows all inbound connections so that we can connect to the database from anywhere. We will be using MySQL version 5.7.30 which is compatible with WordPress latest version.
Once the processes id finished the Database will be created.

Step 3: Installing the WordPress and httpd server on the EC2 instance

Now, let's get back to EC2 and connect to the the instance we launched earlier. Once this is done run the following command:
$ yum install httpd php -y

Download WordPress Software using :
$ curl https://wordpress.org/latest.tar.gz --output wordpress.tar.gz

Once WordPress is downloaded follow the following steps:

Unzip the downloaded WordPress tar file
$ tar xf wordpress.tar.gz

Go to WordPress directory and copy all the content of that directory to the /var/www/html directory
$ cd wordpress

$ cp -r * /var/www/html/
$ systemctl start httpd
$ systemctl status httpd

Now Start the httpd services :
$ systemctl start httpd
$ systemctl status httpd

Now Start the httpd services :
$ systemctl start httpd
$ systemctl status httpd


Step 4: Go to the EC2 instance and copy Public IP to access the WordPress server

Then you will reach the page where the WordPress has been launched.
Now the next step is to provide all the required Database credentials and then your WordPress will be setup successfully.


Thanks for reading, Happy learning!
