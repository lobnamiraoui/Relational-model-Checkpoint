Hotel Management Database Project Introduction This project is a database system designed to manage a hotel chain's data efficiently. It incorporates tables for hotels, rooms, categories, employees, and room types to capture all essential aspects of hotel operations. The system uses relational modeling and adheres to normalization principles for data consistency.

The database supports the following operations:

Managing hotel data and their respective rooms.

Defining room categories, types, and pricing.

Associating employees with hotels and tracking their roles.

Creating hierarchical employee relationships (managers and staff).

ER Model Overview The entity-relationship model provided for this project has been converted into a relational model. The relational schema was constructed using PlantUML to visualize relationships and dependencies.

Database Schema The schema includes the following tables:

Hotel Stores information about the hotels.
Columns:

Hotel_Id (Primary Key)

Hotel_Name

Type Defines the types of rooms available in the hotels.
Columns:

Type_Id (Primary Key)

Type_Name

Room Captures details about individual rooms in a hotel.
Columns:

Room_Id (Primary Key)

Floor

Hotel_Id (Foreign Key referencing Hotel)

Type_Id (Foreign Key referencing Type)

Category_Id (Foreign Key referencing Category)

Category Defines room categories and associated pricing.
Columns:

Category_Id (Primary Key)

Category_Name

Price

Beds_Numbers

Employee Manages employees and their hierarchical relationships.
Columns:

Employee_Id (Primary Key)

Employee_Name

Employee_Speciality

Hotel_Id (Foreign Key referencing Hotel)

Manager_Id (Self-referencing Foreign Key to track managers)