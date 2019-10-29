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
The routes in create_router.js and the path passed to it in server.js
2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
The server is responsible for communicating with the database and setting the routes for the client to access the data. The client side deals with the user interface and how that communicates with the server.
3. What are the the responsibilities of server.js?
It sets up the database, sets up the connection to the port on the browser, and accesses the routes in create_router.js.
4. What are the responsibilities of the `gamesRouter`?
It defines how get, post, put and delete requests to the server are treated.
5. What process does the the client (front-end) use to communicate with the server?
Get, post, put and delete requests using the functions defined in GamesService.js.
6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
The second argument is an object that contains optional instructions for the request. In this app it is used to set the type of request to POST or DELETE as appropriate, and to format the content of the POST request.
7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
Get, create and destroy.
8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
To allow server.js to communicate with the Mongo database.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Add to your diagram the dataflow for removing a game.
