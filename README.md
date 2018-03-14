# ToDoList Node.js REST API Learning by doing
My first project with node.js trying to learn by doing.

## What am i using?
Express - for creating a server.
Nodmon - keep track of changes to our application by watching changed files and automatically restart the server.
Mongoose - for interacting with MongoDB(Database) instance.
bodyParse - Parse incoming request bodies in a middleware which could be used to return more interactive messages.
Middleware - basically intercepts incoming http request and as such you can use them to perform several operations ranging from authentication to validating etc.

### Project Architecture

controllers - five different functions(list_all_tasks, create_a_task, read_a_task, update_a_task, delete_a_task). For the routes. Each of this functions use different mongoose methods such as find, findById, findOneAndUpdate, save and remove.

models - using mongoose we create a model of how our collection should look like. Task collection(table) will contains a name: a string, and date it was created. It also contains task status which we have defined as panding - a default value for every task created.

routes - routing refers on how our application responds to a client request for a specific endpoint, which is a URI(or a path) and a specific HTTP request method (GET, POST, and so on). Each of the routes have different route handler functions, which are executed when the route is mathced.

'/tasks' - methods 'GET' and 'POST'
'/tasks/taskId' - methods 'GET', 'PUT', 'DELETE'

We required a controller so each of the routes methods can call it's respective handler function.

### Start the project

Start MongoDB

```
mongod
```

Start server

```
npm run start
```

