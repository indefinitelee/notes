Promises

A promise is an object that may produce a single value some time in the future: either a resolved value, or a reason that it’s not resolved (e.g., a network error occurred). A promise may be in one of 3 possible states: fulfilled, rejected, or pending. <sup>[1](#1)</sup>

Native JavaScript promises don’t expose promise states. Instead, you’re expected to treat the promise as a black box. Only the function responsible for creating the promise will have knowledge of the promise status, or access to resolve or reject.<sup>[1](#1)</sup>

Here is a function that returns a promise which will resolve after a specified time delay: <sup>[1](#1)</sup>
```
const wait = time => new Promise((resolve) => setTimeout(resolve, time));

wait(3000).then(() => console.log('Hello!')); // 'Hello!' 
```
rewritten: 
```
const wait = function (time) {
 new Promise ( function (resolve) {
  function() setTimeout(resolve, time)
   }
  }
 ```

Sources:

#1. https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-promise-27fc71e77261
