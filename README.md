# ksu_cms
GUI for IT4983 - Spring 2019


 
Web Application Design Document - Outline
1.	Web Application Overview
1.1	Purpose & Functionality
2.	Wireframe
2.1	Home / Project Overview Page
2.2	Project Page
2.3	Upload Page
3.	Development
3.1	Development Tools
3.2	Languages & Software
4.	Requirements
4.1	 Basic Requirements
4.2	Detailed Requirements
5.	Design
5.1	Front-End – GUI Design
5.2	Back-End – Database Design
5.3	User Login
5.4	JavaScript & PHP Implementation 
1.	Web Application Overview
1.1	Purpose & Functionality
The goal of this Capstone Project Progress Tracking is to create a web application to track Capstone projects. Sponsors, professors and students will be able to view the projects within the class.

The team will provide the IT department with a web-based sub-system for better management of the capstone projects progress tracking. This project is one part of a larger capstone project management system. This part should be able to assemble/integrate with other teams to help the IT department manage the capstone process. 

This project utilizes HTML and CSS, we will use Material Boot Design for creating each web page. The web application will be hosted on Windows Server. The web app will allow students to submit a weekly progress summary. Additionally, allowing the instructor and project sponsor to view the weekly summary and write comments. This project should be completed by the end of this semester, in the beginning of May.

2.	Wireframe
2.1	Home / Project Overview Page
 ![image](https://user-images.githubusercontent.com/12768804/213250753-dbf3b61f-ba82-4334-b1b5-a71dfd4511c9.png)

2.2	Project Page
 ![image](https://user-images.githubusercontent.com/12768804/213250794-dc7dff61-3975-436e-af15-11a8f6171eaa.png)

2.3	Upload Page
 ![image](https://user-images.githubusercontent.com/12768804/213250822-a0a74f47-d082-4313-b428-5f71f5631a30.png)

3.	Development
3.1	Development Tools
To design, test and implement this web application; we will be using a variety of tools with specific functionalities. Below are a list of the tools and the functionalities they provide.
•	Adobe Dreamweaver CC 2019 – Designing the web application.
•	Angular CLI – 
•	MySQL – Creating database tables and storing values using relationships.
•	Windows Server – Used to host the web application.
•	Virtual Machine – Provided by Kennesaw State University for testing the web application.

3.2	Languages and Software
The following are a list of languages we will be using to design and program the web application. A short description will be included aside each language based on its functionality within this project.
•	HTML & CSS – Designing web application pages.
•	JavaScript – Used for manipulating the CSS within the HTML code.
•	PHP – Used for communication and functionality between the web form and database.
•	SQL - Creating database tables and storing values using relationships.

4.	Requirements
4.1	Basic Requirements
Main page
•	Projects should be contained in the main page as “widgets”
•	Each widget will contain basic project information and status
Project page
•	Separate page (redirect) after ‘More Information’ on a project widget is clicked
•	Contain more detailed information about the project status
o	Project overview (requirements)
o	Update project status
o	View submissions (in list format – newest submission on top)
o	Make comments on submissions (professor view)
Upload page
•	Form allowing users to:
o	Select a project (professor view)
o	Update project status
o	Submit required documents
o	Make comments on submissions (student view)
o	Type weekly report

4.2	Detailed Requirements
One of the detailed requirements of this web application is the ability to see if a project is ‘On Track’, ‘In Progress’ or ‘Not on Track’ based on a color scheme. The color scheme is designed represent the project’s current status. This color scheme will be used on the project overview (home page) and the color will be displayed on the bottom of each project widget (see image below).
This color will be updated based on the option chosen by the project sponsor, professor or team leader – on each individual project page or via the ‘Upload’ form.
•	Green – On Track
o	Project is up-to-date
o	Everything has been submitted on time
•	Yellow – In Progress
o	Requires an update
o	Requirements missing (documents / weekly report)
•	Red – Not on Track
o	Requires an update
o	Nothing submitted
o	A week (or more) behind
 ![image](https://user-images.githubusercontent.com/12768804/213250887-9aef6219-18d8-41ac-9f27-f0d96a9ed701.png)


5.	Design
5.1	Front-End – GUI Design
The front-end GUI is designed for simplicity and functionality. The index/project overview page was made for quick access to all projects and understanding the project status at a glance. After a user has successfully logged in, they will be redirected to the index page where they can click on a project widget and be directed to the project’s dedicated page.
Each dedicated project page will contain the project’s information such as the project’s title, sponsor name, technical skills required, duties of the student, etc. The information on each project page is pulled from the back-end database and auto-filled in its respected section on the page. Additionally, for each project there will be quick access to updating the project status to one of the following: on track, in progress, or not on track. The selection of the status will, in turn, update the project’s widget color on the index page to the respected color of the project’s status.
We have also implemented a web form page that is used to choose a project (professor view), upload/submit required documents, update a project’s status, and manually type comments for a submission (professor and student).
In the future, students who view the web form (Upload) page should have their project automatically chosen from the dropdown box. Students should not have access to other projects apart from their own. The same goes for the index page; students should only be able to view their project page and no others.
5.2	Back-End – Design
The backend is based on Windows Server. Windows Internet Information Services (IIS) hosts and manages the website. MySQL Database is used to store information regarding projects and updates. In the website, several different languages are used to make it function correctly. The based of the website is composed of HTML and CSS. Pieces of the site, such as the navigation bar and footer, are imported into each page with JavaScript. Each page communicates with the database using PHP.
5.3	User Login
The user login functionality is not a requirement for our part of this project. This feature is expected to be added in the upcoming semesters.
The user login page should be a standard page with a textbox for the username and password. Once the user clicks the ‘Log In’ button; the username and password should be sent to the backend database and verified. If this login is successful, the user should be redirected to the index/project overview page. If the login is unsuccessful, a failed login message should appear on the login page.
All students and the professor are expected to receive logins in the upcoming semesters. Each user can log out of their account by selecting the ‘Account’ option in the navigation bar and choosing ‘Log Out’. The user will then be logged out of the system and redirected back to the login page.
5.4	JavaScript & PHP Implementation
JavaScript will be used to change the color of a project widget according to the option chosen for each project status. For example, if the option ‘On Track’ is chosen for a project status – JavaScript should communicate with the index/project overview page to change the color of the widget associated with that project.
PHP will be used for the communication between the ‘Upload’ page and the back-end database. Specifically, PHP will be used to upload documents to the database and display these documents on their respected project page. Additionally, the same will apply for comments (on submissions) and weekly reports typed on the ‘Upload’ page.
