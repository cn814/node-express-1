### Conceptual Exercise

Answer the following questions below:

- What are some ways of managing asynchronous code in JavaScript?
callbacks, promises, and async/await keywords

- What is a Promise?
A Promise is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason

- What are the differences between an async function and a regular function?
When a normal function is executed, it runs sequentially . That is, if you have two functions A () and B () and execute them in that order, the B () function will only be called when the A () function finishes its execution.

By contrast, if you have an asynchronous function A () (for example, that performs an I / O operation or other blocking operation), it can be called and while the operation is performed you can execute another function B () ( asynchronous or not) in the main context. Later, the A () function will return its value when the operation is finished and the main thread is available for that.

- What is the difference between Node.js and Express.js?
NodeJS is an event-driven, non-blocking I/O model using JavaScript as its main language. It helps to build scalable network applications. Express is a minimal and flexible Node. js web application framework that provides a robust set of features for web and mobile applications.

- What is the error-first callback pattern?
The error-first pattern consists of executing a function when the asynchronous operation ends (such as an incoming AJAX response) which takes as first argument an error, if one occurred, and the result of the request as extra arguments.

- What is middleware?
Middleware is a software that acts as an intermediary between two applications or services to facilitate their communication.


- What does the `next` function do?
The next function is a function in the Express router which, when invoked, executes the middleware succeeding the current middleware

- What are some issues with the following code? (consider all aspects: performance, structure, naming, etc)

```js
async function getUsers() {
  const elie = await $.getJSON('https://api.github.com/users/elie');
  const joel = await $.getJSON('https://api.github.com/users/joelburton');
  const matt = await $.getJSON('https://api.github.com/users/mmmaaatttttt');

  return [elie, matt, joel];
}
```
