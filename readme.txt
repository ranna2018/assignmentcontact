Project Description: 

This project is developed to maintain the contact information. With this project you will be able to add 
contact details such as First Name, Last Name, Email, Phone Number along with status ( by default status will be active, unless it is changed during the data entry process).

Technical aspects:
This project is developed using .NetCore WebApi Version 2.1.4, SqlServer 2016 express edition and Angular 6.0.8. Visual Studio Code IDE is used to develop this project

Database:
Sql Server 2016 is used as data a store for this project. script "SQL_Contact_Scripts.sql" has the DDL statements to store data into the contact table. Please run this script.

.NetCore WebApi and Angular:
This project has following structure - 
HiringApi - HiringApi has the restful services which are exposed at url end point - "http://localhost:5000". These end points will inturn make call to HiringServices to get the contact information data, save and update. 

HiringServices is the place where implementation of database calls, interfaces and view models are defined. Which inturn uses entitiy models from HiringCore project.

HiringCore project has the entities and database context and logging contexts.

HiringWeb project is the angular project for front end to be able to perform add, update or edit contact information along with getting list of contacts.

Log folder will have application error logs.

To run the project, you will need following:

1)	NodeJS V8.11.1 
2) 	Angular CLI 6.0.8
3) 	.NetCore 2.1.4

Setup the project:
Please note that with this project has all the dependent files are included within such as nodemodules...
Change the connection string: Please navigate to HiringApi->appsettings.Development and appsettings.Production(both places) and replace username (AAAAA) and password (BBBBB) provided in the connection string and also make sure to change the data source name appropriately. Now at the command prompt navigate to "HiringApi" and issue command "dotnet run". This command will ensure to run selfhosted service at localhost:5000 and you will see "Now listening on: http://localhost:5000"

Open another command prompt and navigate to HiringWeb and issue "ng serve", wait until you see "compiled successfully". Now angular will continue to listen to localhost:4200.

Now, Open the browser and go to http://localhost:4200

You will see splitmenu -> Add and Show
Add -> is to be able to add the contact information
Show -> is to list the all the contacts
Within the show there are two action links Edit and Delete
Edit -> will allow you to already entered contact information
Delete -> will just inactivate the contact but you will still see in the contact list.


