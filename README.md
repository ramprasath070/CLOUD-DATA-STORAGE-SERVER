# CLOUD-DATA-STORAGE-SERVER

### NAME: RAM PRASATH S
### REG NO: 212224040266

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
<img width="1916" height="1143" alt="Screenshot 2026-11-11 103830" src="https://github.com/user-attachments/assets/86e5eb82-d70f-4790-a5f4-dc2ab6c60570" />
<img width="1911" height="1096" alt="Screenshot 2026-11-11 104111" src="https://github.com/user-attachments/assets/ee80a683-ce10-43d6-b3be-18eeaac3efaf" />
<img width="1916" height="1148" alt="Screenshot 2026-11-11 105009" src="https://github.com/user-attachments/assets/2067af49-9e4e-4941-8664-5afff0504e88" />
<img width="1915" height="1102" alt="Screenshot 2026-11-11 105423" src="https://github.com/user-attachments/assets/9e3b52bf-6db3-4695-98eb-9740c708aaa2" />
<img width="1908" height="637" alt="Screenshot 2026-11-11 112311" src="https://github.com/user-attachments/assets/dd7bf95b-26d3-4f00-a504-a778ab1782a7" />

## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.

