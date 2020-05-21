# webapp-flask

This is a simple web application using [Python Flask](http://flask.pocoo.org/) and [MySQL](https://www.mysql.com/) database. 
This is used in the demonstration of development of Ansible Playbooks.
  
  Below are the steps required to get this working on a base linux system.
  
  - Install all required dependencies
  - Install and Configure Web Server
  - Start Web Server
   
## 1. Install all required dependencies
  
  Python and its dependencies

    apt-get install -y python python-setuptools python-dev build-essential python-pip python-mysqldb

   
## 2. Install and Configure Web Server

Install Python Flask dependency

    pip install flask
    pip install flask-mysql

- Copy app.py or download it from source repository
- Configure database credentials and parameters 

## 3. Start Web Server

Start web server

    FLASK_APP=app.py flask run --host=0.0.0.0
    
## 4. Test

Open a browser and go to URL

    http://<IP>:5000                            => Hello Everyone
    http://<IP>:5000/how%20are%20you            => ITE BHOPAL !
    
    
## 0. Lab
yum install git -y
git clone https://github.com/sonulodha/webapp-flask.git
cd webapp
ls
docker build -t mitrasonu/webapp
docker push mitrasonu/webapp
docker images
docker run --name app1 -p 8080:8080 mitrasonu/webapp
docker ps 
firefox ip:8080
