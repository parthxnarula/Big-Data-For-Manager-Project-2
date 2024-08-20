# Big-Data-For-Manager-Project-2

**Driving License Form Database Project**

*Overview*

This project is focused on designing and implementing a database to manage data related to driving license applications. It includes tables for applicants, addresses, licenses, medical certificates, and driving schools. The project also implements user roles and access control to manage different levels of permissions within the database.

*Project Structure*

*1. Entity-Relationship Diagram (ERD)*
A visual representation of the database schema, showcasing the relationships between entities like Applicants, Addresses, Licenses, Medical Certificates, and Driving Schools.

*2. SQL Schema*
*Database Creation:*
The database DrivingLicenceDBS is created using SQL.
*Tables:*
Applicants: Stores information about applicants including their personal details.
Addresses: Contains addresses linked to the applicants.
Licenses: Holds data about the licenses issued, including license number, vehicle class, and expiration details.
MedicalCertificates: Manages the medical certification details associated with the applicants.
DrivingSchools: Records information related to driving school certifications.

*Sample SQL Commands:*
Example SQL code for creating the tables is provided. Here is a sample of the Applicants table creation:
sql
Copy code
CREATE TABLE Applicants (
  ApplicantID INT PRIMARY KEY AUTO_INCREMENT,
  FirstName VARCHAR(50),
  MiddleName VARCHAR(50),
  LastName VARCHAR(50),
  DateOfBirth DATE,
  Gender VARCHAR(10),
  Email VARCHAR(100),
  MobileNumber VARCHAR(20),
  LandlineNumber VARCHAR(20)
);
Insert Statements:
SQL commands to insert sample data into each table are included. This helps simulate real-world driving license application processes.
Example insert into the Applicants table:

*3. User Roles and Access Control*
User Creation:
The database includes the creation of users with different roles:
AdminUser: Has full access to all tables in the database.
DataEntryUser: Has permissions to insert and update records in specific tables.
ViewerUser: Has read-only access to all tables.
Privilege Management:
Example SQL code to grant privileges:

GRANT ALL PRIVILEGES ON DrivingLicenceDBS.* TO 'AdminUser'@'localhost';
INSERT INTO Applicants (FirstName, MiddleName, LastName, DateOfBirth, Gender, Email, MobileNumber, LandlineNumber) 
VALUES ('John', 'Michael', 'Doe', '1990-01-01', 'Male', 'john.doe@example.com', '1234567890', '0123456789');

*4. User Roles and Access Control*
User Creation:
The database includes the creation of users with different roles:
AdminUser: Has full access to all tables in the database.
DataEntryUser: Has permissions to insert and update records in specific tables.
ViewerUser: Has read-only access to all tables.
Privilege Management:
Example SQL code to grant privileges:

GRANT ALL PRIVILEGES ON DrivingLicenceDBS.* TO 'AdminUser'@'localhost';

*5. Project Submission*
Submitted To:
Prof. Ashok Harnal
Submitted By:
Manish Mrityunjay Mohapatra (045029)
Parth Narula (045039)
Rahul Gohri (045044)

*How to Use*
*Setup Database:*
Clone the repository and execute the provided SQL scripts to create the DrivingLicenceDBS database and the associated tables.
Use the insert statements to populate the tables with sample data.

Manage User Roles:
Use the SQL scripts to create users and assign them appropriate roles within the database.
AdminUser has full privileges, DataEntryUser has insert/update privileges, and ViewerUser has read-only access.

Assumptions
This project assumes the user has a basic understanding of SQL and database management.
The roles and permissions are structured to reflect typical operations within a driving license management system.
