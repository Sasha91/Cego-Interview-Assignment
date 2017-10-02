# Cego-Interview-Assignment
## Made by Sasha Junker

## General information
My relfections on this task will be very biased from the experiences i have in webdevelopment through AngularJS and ASP.NET RESTful API's. It's made with the html framework, Bootstrap, and PHP on a local wamp server and MySQL database.

My solution consist of two files besides. 
- index.php 
- QueryManager.php

The only file that is shown is the index.php which including methods from QueryManager.php in order to structure the content of index.php. It calls a single function which checks if the server have recieved a post request of the name "sql", and if so, it makes contact with the database and executes the query.

If the query is succusful, a download button will be shown that allows the user to download a txt file, containing the result of the query. Whatever the query returned will be removed from the database.

## Security
Executing a "random" query on the database is never a good idea, as it might contain malicious instructions, such as "drop table uers". From my previous experience, all query execution on a database is strictly handled by the server API which will have to verify any input that is passed to the query through the API endpoints.

## Testing
Testing of API's is usually done through unit tests and end-to-end tests. Monkey tests can be performed on the UI and several testing frameworks, such as Jasmin, exists for testing the javascript.

## Next steps
I would personally always to try to create a seperate API with specific controlled endpoints. A possible solution to obtain greater security could be to make a specific set of commands and table in the database that the user can access, instead of being in full control.

A nicer UI and a front end framework that allows a layered structure would make it easier to expands the application in the future.
