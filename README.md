Database Model for Guvi Zen Class with dbdiagram.io
This guide provides step-by-step instructions and guidelines for creating a database model using dbdiagram.io, a popular online tool for designing database schemas.

Getting Started
Access dbdiagram.io
Open your web browser and visit dbdiagram.io.
Sign In or Create an Account
If you already have an account, sign in. Otherwise, create a new account to save your work.
Designing Your Database Model
Create a New Diagram
Click on the "Create New Diagram" button.
Give your diagram a name, such as "Guvi Zen Class Database Model."
Add Tables
Click the "Table" icon to add tables to your diagram.
Name your tables to reflect the entities in your database model.
Add Columns
Inside each table, add columns to define the attributes of your entities.
Specify the data type for each column (e.g., INT, VARCHAR, DATE).
Indicate primary keys, foreign keys, and unique constraints.
Establish Relationships
Use lines to connect tables and define relationships (one-to-one, one-to-many, many-to-many).
Label the relationships to clarify their nature.
Example Tables and Relationships for Zen Class Database
Students Table
Column	Type	Constraints
studentid	INT	Primary Key, AUTO_INCREMENT
studentname	VARCHAR(255)	
mobilenumber	VARCHAR(255)	UNIQUE
email	VARCHAR(255)	UNIQUE
mentorname	VARCHAR(255)	
batchid	INT	
batchname	VARCHAR(255)	
Tasks Table
Column	Type	Constraints
taskid	INT	Primary Key, AUTO_INCREMENT
taskname	VARCHAR(255)	UNIQUE
studentid	INT	
mentorid	INT	
mentorname	VARCHAR(25)	
batchname	VARCHAR(50)	
Mentors Table
Column	Type	Constraints
mentorid	INT	Primary Key, AUTO_INCREMENT
email	VARCHAR(50)	UNIQUE
contactno	VARCHAR(15)	UNIQUE
assignedbatch	VARCHAR(100)	
Batches Table
Column	Type	Constraints
batchid	INT	Primary Key, AUTO_INCREMENT
batchname	VARCHAR(255)	
totalstudents	INT	
mentorid	INT	
Queries Table
Column	Type	Constraints
queryid	INT	Primary Key, AUTO_INCREMENT
querytext	TEXT	
studentid	INT	
mentorid	INT	
Dashboards Table
Column	Type	Constraints
dashboardid	INT	Primary Key, AUTO_INCREMENT
studentid	INT	
mentorid	INT	
batchid	INT	
Mock Interviews Table
Column	Type	Constraints
mockinterviewid	INT	Primary Key, AUTO_INCREMENT
studentid	INT	
mentorid	INT	
batchid	INT	
Foreign Key Relationships
The students table references the batches table via batchid.
The tasks table references the students table via studentid.
The tasks table references the mentors table via mentorid.
The batches table references the mentors table via mentorid.
The queries table references the students table via studentid.
The queries table references the mentors table via mentorid.
The dashboards table references the students table via studentid.
The dashboards table references the mentors table via mentorid.
The dashboards table references the batches table via batchid.
The mock_interviews table references the students table via studentid.
The mock_interviews table references the mentors table via mentorid.
The mock_interviews table references the batches table via batchid.
Exporting Your Model
Export as SQL or Image
Once your model is complete, export it as SQL code and as an image.
You can use the generated SQL code to create your database schema.
Sharing and Collaboration
Share Your Diagram
Share your diagram by clicking the "Share" button and providing collaborators with the link.
Click here to view this db design: Guvi Zen Class Database Model

Happy modeling!
