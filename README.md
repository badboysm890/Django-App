# Django-App
CURD Operations


Git clone the project

pip install -r requirement.txt

python3 manage.py migrate

python3 manage.py runsever

check in the 127.0.0.1:8000


AWS Upload Guide

https://aws.amazon.com/
go to this link and login

next https://ap-south-1.console.aws.amazon.com/ec2/v2/home?region=ap-south-1#Home:

now next 

CLick on "launch instance"

Now select Ubuntu 16.04 LTS
and 
click select

Next click review and launch

Click on edit Security Group 

click on Select Existing security group

Now it ready click on LAUNCH

Now again click launch

Important Stuff !!!

It will ask you for the value Key Pair for download

On First Drop Down select "Create a New Key Pair"

and type any name and click Download Key Pair


Key Pair (Its very important to connect to your instance)



Now after download click on launch instances

Wait for few Mins for the instance to be ready.


Now again go to EC2 by using this link

https://ap-south-1.console.aws.amazon.com/ec2/v2/home?region=ap-south-1

Click on 

https://ap-south-1.console.aws.amazon.com/ec2/v2/home?region=ap-south-1#Instances:


Now you will have your Instance running there 

select the instance you created

Now on the top after clicking on the intance you have created 

Click on connect

There it will show how to connect to you instance Follow the instruction Carefully which will connect to the instances



If on windows use Connect Using Putty Options

Follow amazon instance connection instruction 

After Connecting sucessfully

in the putty shell (Which is ubunutu terminal using ssh)

Now 

type in terminal the following


sudo apt-get update

sudo apt-get install python3

sudo apt-get install python3-pip

pip3 install django 

sudo apt-get install mysql-server

define your password when it prompts for the password

systemctl start mysql

systemctl enable mysql

/usr/bin/mysql -u root -p         ("it is used to start the mysql server")

after typing password

now in mysql cli

UPDATE mysql.user SET authentication_string = PASSWORD('password') WHERE User = 'root';

replace password with any password you want

FLUSH PRIVILEGES;

Now thats it setup django and make migrations and everything will work as needed


