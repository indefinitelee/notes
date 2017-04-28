#Promises

A promise is an object that may produce a single value some time in the future: either a resolved value, or a reason that it’s not resolved (e.g., a network error occurred). A promise may be in one of 3 possible states: fulfilled, rejected, or pending. <sup>[1](#1)</sup>

Native JavaScript promises don’t expose promise states. Instead, you’re expected to treat the promise as a black box. Only the function responsible for creating the promise will have knowledge of the promise status, or access to resolve or reject.<sup>[1](#1)</sup>

A promise can be:<sup>[2](#2)</sup>

* fulfilled - The action relating to the promise succeeded
* rejected - The action relating to the promise failed
* pending - Hasn't fulfilled or rejected yet
* settled - Has fulfilled or rejected

Here is a function that returns a promise which will resolve after a specified time delay: <sup>[1](#1)</sup>
```
const wait = time => new Promise((resolve) => setTimeout(resolve, time));

wait(3000).then(() => console.log('Hello!')); // 'Hello!' 
```
###Rewritten in ES5: 
```
var wait = function wait(time) {
 return new Promise ( function (resolve) {
  return setTimeout(resolve, time)
   }
  }
 ```

Sources:

#1. https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-promise-27fc71e77261
#2. https://developers.google.com/web/fundamentals/getting-started/primers/promises
#3. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
