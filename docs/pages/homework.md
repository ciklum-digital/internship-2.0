# Homework
Hi, welcome to the Homeworks section!

Your homeworks will be based on extension and enhancement of your test task. So please, make sure it is deployed to Github Pages in order to make it possible for our mentors to check it after every lecture.

Good luck and enjoy your practice time!
## Homework 1
Ok, so for your test task you had several users in our system. Let's upgrade them to the next level this time. Now you would need to create two Classes User (base class) and Admin (should be inherited from User). 

### Requirements:
 - Each team member should belong either to User class or Admin class.
 - When user opens an application he/she has to authorize himself using the select modal (like in the example mockup).
 - If authorized user is Admin he is able to create and update events(if Drag and Drop was implemented in your test task).
 - If authorized user is User he/she is not able to create/update events. This means that 'Create Event' button should be hidden for those users.

### Additional requirements:
- Please make sure your application meets the ES6 standard and uses all ES6 features where it is appropriate and possible.
 
 ![Basic_calendar](../assets/images/homeworks/hw-1-1.jpg)
 
## Homework 2
Ok, so for your test task you stored all your Events in localStorage. Now you need to implement CRUD operations for events. We have created small server to store Events.

You can find API documentation here: http://158.101.166.74:8080/swagger/index.html

API endpoints have next parameters:
 - *system* - it should be applicant's firstname and lastname, for example for John Doe use 'john_doe';
 - *entity* - entity name, in our case should be 'events';
 - *id* - unique identifier that will be created by API automatically.

### Requirements:
 - All Events should be stored on BE side
 - For communicating with API you may use Fetch, Axios etc...
 - Implement create Event via POST method - http://158.101.166.74:8080/api/data/{system}/{entity}

        Example of payload:
        ```
         {
           data: **Data in JSON format**
         }
        ```
 - Implement delete Event via DELETE method - http://158.101.166.74:8080/api/data/{system}/{entity}/{id}
 - To retrieve all Events use GET method - http://158.101.166.74:8080/api/data/{system}/{entity}
 - If you have drag'n'drop you should update Event via PUT method - http://158.101.166.74:8080/api/data/{system}/{entity}
 - For each API call implement Notification that indicates a successful response.

### Optional requirements:
 - Please use async/await for handling API responses
 - Store users in API (create separate *entity* called 'users' and retrieve them via GET method)

