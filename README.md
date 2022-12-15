# ToDo List Task Management application 

## Example accounts 

### FAO Code Institute Assessor
For the purposes of examination 3 example accounts have been created for the attention of the code institute assessor.There is also the option to register a new account with the database which would be the inital action of a first time user.Enjoy! 

1. Username = **paul**     password = **soapstone**
2. Username = **Barry**    password = **plmoknqazwsx12345**
3. Username = **mary**     password = **sandstone**

	---
## UX Overview

### Brief
This website has been created as a way to create, read, update and delete tasks and to enable users from any location to view and upload their own tasks to a community site.

The objectives are to:

1 - provide a service for task management

2 - Enable users to:

* Record and prioritize a list of tasks
* Create their own tasks
* Edit and delete their own tasks
* Quickly return a list of tasks based on search criteria
* Complete tasks by marking them as sucessfully finished

3 - Provide a visually appealing environment for users to encourage others to use the site 

### User Stores
Consideration has been given to the needs of prospective users of the website:

Users are likely to fall into three categories. Users will be:

1 - looking for one off task completion tools

2 - wanting to keep a record of multiple tasks

3 - creating a list of tasks to refer to back to on repeat occasions

#### I want to prioritze a series of tasks
- I would like to make a list:
    - by apponintment type 
    - containing specific dates and times
    - that can be recorded and completed
    - new lists can be generated
    - acess to a calendar     

#### Wanting to share knowledge
- I would like to be able to:
    - add my tasks to the site
    - provide details about the completion status, date, time and importance
    - easily edit my tasks
    - delete tasks that I no longer need

#### Creating a list 
- I would like to find tasks by the individuals who have uploaded them
- I would like to bookmark tasks to create a personal list 
- Create search list of tasks matching certain criteria and sort them by relavance

### Purpose
This website is designed as an interactive front end website with a neat appearance and clear buttons to enable users to easily navigate around the site and to achieve their aims such as those listed above.

Users' tasks are stored in a ***ElephantSQL*** PostgreSQL database accessed via ***Python*** backend code.

Full functionality to enable a user to create a unique profile and password has been implemented.

To access the full functionality of the site a user must 'register' before they can add, edit or delete tasks.

A user can can only acess tasks associated with their account, you will not be able to access the task lists of other users.

The site comprises of 5 pages that can be accessed from the main navigation bar and back buttons  on the site.

The main navbar is displayed on all pages for ease of access to all pages in the site.

#### Add task
The option to add tasks is only displayed in the navigation bar if the user is logged in.
This page can be accessed by the Add tab 'plus' symbol in the navigation bar.
On loading this page displays a form that can be populated by the user with all information about the task they intend to upload.
Required fields are:
- Name of Task
- Description of Task
- Completion status of the Task

The user can add the recipe to their list of favourites (or filtered searching, above) by clicking the star. Clicking again will remove the recipe from the list of favourites.

#### Edit task
The option to edit tasks is achieved by clicking on the task you wish to edit, this will take you to the task update page, which will appear to the user as the same page as the task creation form. Here you can edit your task title, description or completion status. A user may only edit tasks when he/she is logged into their account.

The Edit page can also be accessed directly from the display recipe page, see below.


The user can then return to the main page by clicking the 'submit' button when they have completed their edit or by using the go back button in the navigation bar. It is important to note that using the go back button will not commit your changes to save and so is an opt out option.

#### Delete task
The option to delete tasks is only displayed as a graphic 'X' availble only to logged in users on the main task creation page, situated to the left of each task.

After clicking on the delete task icon the user will be brought to a seperate page and asked to confirm his/her choice. This confirmation process is implemented to avoid the possiblility of a mis-click whereby a user could delete a task by mistake and so a two step verification model has been put in place to avoid such an event.

### Setting up our models and database
For this project the chosen framework employed to complete the application is Django. Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design. The database itself itself will be hosted on the clould by ElephantSQL, from which a PostgresSQL database has been deployed.

The main database table has a one to many relationship. Thereby allowing us to have one user and that user can have many items. Also it should be noted the dajango offers us prepopulated tables which will handle the authentication process needed for securing the site, this is very convienient. 

---
## Features
### Existing
* Responsive design for ease of readability on various device sizes
* Collapsible headers and bodies for search/filter options and task results to provide better read format
* Hidden options to prevent users who are not logged in from editting, deleting or adding tasks
* A visual representation of a calendar for reference
* Branded colour co-ordinated style
* Large, obvious buttons to help the user navigate the site
* Functionality for users to Create, Read, Update and Delete tasks from the site

---
## Testing
Code was written through the Gitpod Cloud IDE.
The website has been tested during production on Chrome and then on IE, Safari and Opera browsers.
See additional README document for specific testing undertaken.

## Deployment
The ToDo list task management apllication is deployed using the Heroku platform and can be viewed at https://ivygardens.herokuapp.com/

### Deployment process
A git respository was created through the bash terminal and the the project was committed to the repository using the standard bash commit command.
Commits to the respository were made at each major development stage or as issues were identified and fixed.

The project was then deployed to Heroku through the Heroku online console, using the following steps:
- Having logged into the Heroku platform a new app was created, titled 'ivygardens'.
- A git url was provided by Heroku on creating the app, https://ivygardens.herokuapp.com/

- A requirements.txt file was created through the bash terminal command 'sudo pip3 freeze --local>requirements.txt'
- The requirements.txt file was commited to the local git repository
- A Procfile was created by bash terminal command 'echo web: python app.py > Procfile
- The Procfile was commited to the local git respository
- The local git repository was deployed to heroku via the bash terminal command 'git push heroku master'
- Local environment variables for:
        - IP,
        - PORT,
        - SECRET, and
        - DATABASE_URI
were set using the Heroku console.
The local git repository was also pushed to github:

The project was then deployed to Github:
- A repository titled "ivygardens" was created in Github.
- A URL was supplied by GitHub https://github.com/bariryan/ivygardens
- The local repository was pushed to the remote repository using bash command "git push -u origin master"

The Github and Heroku repositories were linked using the Heroku console tab "Deploy" and selecting the option to connect to Github.

The Github cookbook respository was located and linked to Heroku and the option for automatic deploys selected to ensure the code pushed to Github matched the build on the Heroku platform.

The deployed project can be viewed at https://ivygardens.herokuapp.com/

To edit/run the code locally it is necessary to pull the code from the Heroku or Github repository. However, as the Heroku repository is intended for deployment purposes only it is recommended that the code is cloned from and pushed to the Github repository.

Automatic deployment to Heroku ensures app is built from the latest code pushed to the Github repository.

Other than a standard browser no further software or implementation is required and the site can be accessed at 'https://milestone-3-recipebook.herokuapp.com/'.

To test and run the Python code locally it is necessary to ensure all relevant requirements are installed locally. (Please see requirements.txt for the required libraries.)

All requirements can be installed by navigating to the directory containing requirements.txt and using python bash command:

$ sudo pip3 install –r requirements.txt
The app can then be run by navigating to the root folder and using bash command:
$ python3 app.py

## Validation
* CSS
    * https://jigsaw.w3.org/css-validator/ was used for validation of css code and did not generate significant errors
* HTML
    * https://validator.w3.org/ was used for validation of HTML code. 
   

* Python
    * https://pep8ci.herokuapp.com/https://pep8ci.herokuapp.com/ was used to validate Python code and did not generate any errors.

## Acknowledgements

The greater part of this application, it's aesthetic, fundamental database structure and code logic is credited to Dennis Ivy https://www.youtube.com/c/DennisIvy?app=desktop
Dennis Ivy is a youtube personality and django educator. His detailed tutorial found here https://www.youtube.com/watch?v=llbtoQTt4qw&t=1102s&ab_channel=DennisIvy served as the main inspiration for my task list project. 


