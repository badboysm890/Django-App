# Django-App
CURD Operations


Git clone the project

pip install -r requirement.txt

python3 manage.py migrate

python3 manage.py runsever

check in the 127.0.0.1:8000


EC2 configure for the aws instances


open this link and go to the ec2 instances : 

https://console.aws.amazon.com/ec2/v2/home

note(may require login sometime if time out)


![alt text](https://docs.aws.amazon.com/quickstarts/latest/vmlaunch/images/vm-launch-instance.png)


click on the launch instance and scroll down and click on the ubuntu 18 LTS and any of your choice.
and click next when it ask for the key pair just download the key by creating new key.

and create a instance.

use chmod 400 key_nam.pem(before connecting to the instance)

ssh -i /path/my-key-pair.pem ec2-user@ec2-198-51-100-1.compute-1.amazonaws.com

use the instace detail as given in example above

once connected 

git clone the repo 
and use the floowing scripts


sudo apt-get install python3-pip
pip3 install django
and  
cd "reponame"

and 
python3 manage.py makemigrations
python3 manage.py runserver 0.0.0.0:8080
now use the instace public ip (which is available in the dashboard of the ec2 instance)

use nohup to run python code which will run it for ever
