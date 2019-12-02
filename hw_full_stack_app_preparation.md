# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
The create_router.js file which is linked to the server.js file which has a localhost set up at 3000, the create_router just specifies the full path/routes.


2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
The server is responsible for mongodb and routes of the data + processing the requests/inputs from client, whereas the client is for the front end and loading the eventBus.

3. What are the the responsibilities of server.js?
As mentioned for the app to be able to use mongodb or external database, as well as setting up the routes for a specific pathway. Also allows for both local host 8080 and 3000 to communicate using cors to bypass errors.

4. What are the responsibilities of the `gamesRouter`?
pass information grabbed from mongodb regarding games to the create_router files and make the right CRUD functionality for said games


5. What process does the the client (front-end) use to communicate with the server?
eventBus? loads the info on to EB then uses GamesService class to update/change the payload it passes in?


6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
so you can specify credentials? like which types of method post etc


7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
'http://localhost:3000/api/games/ + routes used in create routes file  

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
Can 'talk' to the db using it? from within the files.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Add to your diagram the dataflow for removing a game.
