# CLOUD-DATA-STORAGE-SERVER

## NAME: DEEPIKA R
## REG NO: 212224040061

## Aim

To create and configure an Amazon Relational Database Service (Amazon RDS) instance as a cloud data storage server, configure the required security settings, connect it to a web application, and perform database operations using the application.

## Algorithm / Steps

1. Create a Security Group for the RDS database.
2. Add an inbound rule to allow MySQL (Port 3306) access from the Web Security Group.
3. Create a DB Subnet Group using two Availability Zones.
4. Launch an Amazon RDS MySQL database instance.
5. Configure the database with the required identifier, username, password, storage, and instance class.
6. Associate the database with the created Security Group and Subnet Group.
7. Wait until the database status becomes **Available**.
8. Copy the RDS endpoint.
9. Open the web application using the provided Web Server IP address.
10. Enter the RDS endpoint, database name, username, and password.
11. Connect the application to the database.
12. Verify the connection by adding, editing, and deleting records in the Address Book application.


## Program

### Security Group Configuration

* Security Group Name: **DB Security Group**
* Inbound Rule: **MySQL/Aurora (3306)**
* Source: **Web Security Group**

### DB Subnet Group

* Name: **DB-Subnet-Group**
* VPC: **Lab VPC**

### Amazon RDS Configuration

* Engine: **MySQL**
* Template: **Dev/Test**
* Availability: **Multi-AZ**
* DB Instance Identifier: **lab-db**
* Username: **main**
* Password: **lab-password**
* Instance Class: **db.t3.micro**
* Storage: **20 GB (General Purpose SSD)**

### Connect the Application

```text
Endpoint : <RDS Endpoint>
Database : lab
Username : main
Password : lab-password
```

After submitting the above details, perform Add, Edit, and Delete operations on the Address Book application.

## Output
<img width="1918" height="910" alt="image" src="https://github.com/user-attachments/assets/373be1c7-2c21-41fa-9b03-6324d3c05738" />
<img width="1919" height="905" alt="image" src="https://github.com/user-attachments/assets/48433615-1cb1-46e0-884e-451a4dae32e3" />
<img width="1714" height="753" alt="image" src="https://github.com/user-attachments/assets/37d7d7b9-2668-48cb-84b2-872857f993c3" />
<img width="1657" height="644" alt="image" src="https://github.com/user-attachments/assets/e227e3f8-3d66-40a1-97cb-db255b630e0a" />
<img width="1661" height="506" alt="image" src="https://github.com/user-attachments/assets/f25c065b-4a71-46a0-9c14-7399fdb487aa" />

<img width="1765" height="796" alt="image" src="https://github.com/user-attachments/assets/400508c9-a944-4cf2-b076-648c02c04e59" />

## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.

