### High-level approach:
Basically the program will first initialized the server using TCP connection
with ssl to wrap the server. After doing that we will first get the login
page and post the password and username to the server to login. Then we will
crawl the website by doing a while loop that stop until we find 5 flags.
If the server is stopped inside the loop, we reinitialized the the socket
and relogin. For every message we got, we extract the status. If it is 200,
we got the urls to futher crawl and record those that has been visited.
If it is 302, we redirect. Else we continue.

### Challenges faced:
One challenge that we faced is that the server always stop after several minutes
which we forget to reinitialized the server during the while loop.

The other challenge we faced is that we have to implement the multi-threading
to complete the task, else it will take more than an hour to get the flags

### Overview of how you tested your code:
We tested directly on our local server 
