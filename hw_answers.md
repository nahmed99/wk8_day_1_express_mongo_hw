### Answers

1. What is responsible for defining the routes of the `games` resource?

create_router.js 

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?

The games_app folder has two main sub-folders; client and server. 

The client is responsible for client-side processing, displaying information for the user to view, and to accept input from the user. Basically, it takes requests from the user and then passes them on to the server to fulfil. There doesn't appear to be any validation of the data that has been entered (-ve figures are also accepted).

The client, with use of CSS, makes the data presentable.

The server is responsible for servicing requests from the client; it creates new games, again without validation. The current list of games is sent back to the client to display. 

The server also 'talks' to the database, requesting CRUD actions as required (by the instructions/requests form the client).


3. What are the the responsibilities of server.js?

Setup connection and listener to the mongo db.


4. What are the responsibilities of the `gamesRouter`?

gamesRouter is a 'handle' to the createRouter function. It is 'used' to access various actions within createRouter.


5. What process does the the client (front-end) use to communicate with the server?

It uses fetch within GamesService.js (which in 'accesses' server's ip addres)


6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs


It uses the second argument to pass details of specific requests to the server. This is an (optional) init object.


7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

- GET
- POST
- DELETE


8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

Drivers are used to allow computer OS' communicate with a particular device. In the case of the mongoDB driver, I expect it will allow the underlying OS (on the server-side) to communicate (effectively) with the mongoDD that is installed on the system. This will be to allow node.js/express.js to access the data correctly. 


Extension
=========

ObjectId is used to identify the specific 'row'/record that is to be processed. It is like the key for that row/record.