Asynchronous is not just an obscure Javascript magicians concept. We need it for a good reason. Take the following example. Both buttons does the same job, an http request is done to get a distant file and then print it. The request is very slow on purpose (the server will wait 5 seconds to respond). One button is a synchronous code and the other button is an asynchronous code. As you can see, when you click on the first button, the user interface just freeze during the code execution. This is because the main thread can't execute the code and refresh the user interface at the same time. When you click on the second button, the main thread finish its job with the user interface and then the code is executed.

@[Why we need asynchronous]({"layout": "aside", "stubs": ["code.html"], "command": "node server.js", "project":"part2"})

The given example use [jQuery](http://jquery.com/) to perform the http request.

In the future, synchronous http requests will be not supported anymore by browsers. Dealing with asynchronous is just a must have in Javascript world.