Why Node js?
Users interacts with System mobile apps 



user intercats with application
applications with servers
servers with databases

with all the above things there ae request and response cycles happens

`Each request will be handeled by a seperate thread Multi thread requests`

1.Each and every request from the user is attached to a new thread in the server
2.that thread will perform a action on the database
3.for every request there is new thread attched to it

which results in exhaustions of the threads 

Limitations of the multithread:
1. If millions of requests are made per second the threads might exhaust and new request should wait
2. When a thread is accessing the certain part of the `resource` it will blocked for the other thread to  perform actions on it.which means other thread has to wait.`exclusive lock` on the `resource`

`How Single thread model works and how it eliminates the multithread model limitations`

1. when the requests are generated an `event` is generated
2.` Event Emitters` will emit those events in to the` Event Queue` in the server
3. These events are executed using the `EVENT LOOPS` which is asingle threaded mechanism
4. These will be allocated to the worker threads present in the `Thread pool` according to their type.
5. Those worker threads will be processed the request `asynchronously`.
6. these event is also called `event driven model` or `single Thread Model`
7. 





