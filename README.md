Project Overview
Purpose
The application is designed to handle the management of applicants, possibly for a job application or a similar scenario where users can submit their profiles, which include personal details and work experiences. It provides functionalities to create, read, update, and delete (CRUD) applicant records.

Key Components
Controllers:

HomeController: Handles basic page requests like the homepage (Index) and privacy information (Privacy). It also handles error responses through the Error action.
MasterDetailsController: Manages CRUD operations for applicants. It includes actions for:
Index: Displays a list of all applicants.
Create: Allows the creation of new applicant records, including handling file uploads for profile photos.
Edit: Allows for editing existing applicant records.
Details: Shows detailed information about a specific applicant, including their experiences.
Delete: Allows for deletion of an applicant record.
Models:

Applicant: Represents an applicant with properties such as personal details and a list of experiences. Includes functionality for handling profile photo uploads.
Experience: Represents a work experience related to an applicant.
Data Context:

MyDbContext: The Entity Framework Core DbContext class that manages the connection to the database and includes DbSet properties for Applicant and Experience entities. This context is used to interact with the database and perform CRUD operations.
Functionality
Applicant Management:

Users can view a list of all applicants.
New applicants can be added with details and an optional profile photo.
Existing applicant details can be edited.
Detailed views of individual applicants are available.
Applicants can be deleted from the system.
File Handling:

Profile photos are uploaded and saved to a designated folder on the server (wwwroot/Images), with unique filenames to avoid conflicts.
Error Handling:

The application includes basic error handling and displays error information when an issue occurs.
How It Works
Views:

The application uses Razor views (not included in the provided code) to render HTML pages for listing, creating, editing, viewing details, and deleting applicants.
Data Operations:

CRUD operations are performed through Entity Framework Core, which interacts with a relational database to manage applicant records and their associated experiences.
File Uploads:

When creating a new applicant, the application handles file uploads for profile photos and saves them to the server.
Dependencies
ASP.NET Core MVC: For building the web application and handling HTTP requests and responses.
Entity Framework Core: For data access and management of the database.
Summary
This project is a basic applicant management system that allows for creating, viewing, updating, and deleting applicant records. It supports file uploads for profile photos and uses Entity Framework Core for data persistence. The application is structured to separate concerns between different controllers and models, making it maintainable and scalable for future enhancements.
