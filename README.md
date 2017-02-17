sample-jersey-sqlite-application
==================================

This is a sample web application that uses Java + Jersey Rest API and database Sqllite.


**Required tools / Framework to run the application
Tomcat
Maven
Java
Sqllite
Eclipse IDE 

Project Files Description
===========================


pom.xml --> Project Model file used during maven build
.java files --> Project src code for table creation, model (Request/Response) & controller's
Create same directory structure to build projects 


Steps to delpoy application on Tomcat

1) Navigate to <<TomcatHome>>/webapps 
2) Copy the war file

Steps to run tomcat server

1) Navigate to <<TomcatHome>>/bin
2) run startup shell file by executing command ./startup.sh --> This will launch the tomcat server 


Steps to run the api's
1) Install rest Client tool on firefox browser
2) Please refer screen shot attached which have restclient & sample calling


Invoke application API'S


1) Create BLOG TABLE interally with given table strcuture.
**************************************************************
Headers:
	Content-Type: application/json
Method: get
URL:
	http://<<serverip>>:8080/SampleJerseyApp/rest/create
Response:200 OK   	

2) Insert records into blog table
**************************************************************
Headers:
	Content-Type: application/json
	
URL:
http://<<serverip>>:8080/samplejerseyapp/rest/post
Method : post

Body:
	{"pid":4,"title":"blog1","body":"test blog"}
Response:200 OK 

3) Retrieve Blog records
**************************************************************
Get Blog request URL:
http://172.30.66.102:8080/SampleJerseyApp/rest/post

Headers:
	Content-Type: application/json

URL:
http://<<serverip>>:8080/samplejerseyapp/rest/post
Method : get
Requset-type:get
Response:
    [
        {
            "body": "Body",
            "id": "1",
            "title": "Paul"
        },
        {
            "body": "test blog",
            "id": "3",
            "title": "blog1"
        }
    ]









