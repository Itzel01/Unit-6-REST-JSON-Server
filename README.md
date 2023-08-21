# Unit-6-REST-JSON-Server:

## Lesson Overview: 
- 00:00 - 00:05 - Review CRUD 
- 00:05 - 00:15 - REST
- 00:15 - 00:30 - REST(ful) APIs
- 00:30 - 00:40 - Request/Response Cycle 
- 00:40 - 01:00 - JSON Server Mini Lab 

## Objectives: 
- Students should be able to:
  - Understand the REST Paradigm
  - Identify REST API's
  - Create examples of REST URLs 
  - Understand the request/response cycle
  - Get started by creating their own REST(ful) API through the use of JSON Server

## Key Questions:
- What is REST?
- What are REST Principles?
- Why do we use REST?
- How can we represent complex relationships with REST?

## Terms To Know:
- **CRUD:** Create, Read, Update, Delete
- **REST:** Representational State Transfer
- **API:** Application Programming Interfaces

## REST API:
REST, or Representational State Transfer, is an architectural style that is meant to make communication between systems easier. With REST, we can separate the client and server! This is because as long as both systems use the same agreed-upon communications, they can work independently from each other; in this case, it would be RESTful conventions. By creating RESTful endpoints, the client and server hit the same endpoints, perform the same actions(CRUD operations), and respond similarly. 

## Request/Response Cycle: 
- A client must first send a request to the server through the RESTful API.
  - A request consists of an HTTP verb, a header, a path, and an optional message body(depending on the verb)!
- The web server will then send a message to the database.
- The database will respond and send back some information to the server.
  - If the request is GET, the database may not change but instead return the information necessary.
  - If the request is POST, UPDATE, or DELETE, the database may respond with the new information!
- The web server, using the RESTful API, will then display a change in the client.

## Example of RESTful Conventions: 

Below is a table that shows the ways in which the specific HTTP method is related to a specific CRUD action. In addition, there is information on the REST convention! The convention is `/pluralNane/:id`. The `id` is only needed when we are specifying which item we are updating. The first 6 items in the table are fairly simple; however, relationships can sometimes be complex, and we will need to show that as well. The last 2 are examples of relationships that are more complex! 

HTTP Method | URL Path | CRUD Action | Result
--- | --- | --- | --- | 
GET | /books | READ | Responds with all books 
GET | /books/:id | READ | Responds with the book that corresponds with that id 
POST | /books | CREATE | Adds a book to inventory and respond with a newly added book
PATCH | /books/:id | UPDATE | Updates the detail of the specific book and responds with the updated book 
PUT | /books/:id | UPDATE | Completely updates the details of a specific book and responds with the new book's information 
DELETE | /books/:id | DELETE | Removes the book from inventory
GET | /authors/:id/books | READ | Responds with all of the books from the specified author
GET | authors/:id/books/:id | READ | Responds with a specified book from the specified author

### Additional Resources: 
- [What is REST?](https://www.codecademy.com/courses/learn-node-js/articles/what-is-rest)
- [Postman](https://learning.postman.com/docs/sending-requests/requests/)
- [JSON Server Documentation](https://www.npmjs.com/package/json-server#getting-started)

### Useful Information to check out: 
- [Making Multiple Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all)
- [Difference between Patch and Put](https://www.geeksforgeeks.org/difference-between-put-and-patch-request/#)
