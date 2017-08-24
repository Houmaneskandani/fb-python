# Facebook in Python
## Introduction
In this project, we will use Mininet to emulate a network topology consisting of one server and three client nodes and implement a simple Facebook application on top of this topology using a client-server model. Clients run client codes to make use of the capabilities they are provided with and server is responsible for authenticating users, receive posts and messages form users and send and display them for the proper intended users
## Features
* Whenever a user connects to server, he should be asked for his username and password.
* Username should be entered as clear text but passwords should not (should be either
obscured or hidden).
* User should log in successfully if username and password are entered correctly. A set of
username/password pairs are hardcoded on the server side.
* User should be provided with a menu. The menu includes all possible options (commands)
user can use and how he can use them. These options include Logout, Change Password,
etc.
* Change Password: User should be able to change his password. To do this, old and new
passwords should be entered (neither as clear text).
* Logout: User should be able to logout and close his connection with the server.
* Send Message: A user should be able to send a private message to any other user (whether or not the recipient of the message is online).
A user should see the number of unread messages when logging in.
* See Unread Messages: A user should be able to read all unread messages.
* A user should see his messages in real-time (live) if he is online when someone sends him a messages.
Send Friend Request: A user should be able to send any other user a friend request.
* A user should see the number of unanswered received friend requests when logging in.
* Respond to Friend Request: A user should be able to see all friend requests and decide on
them one by one (with Accept or Reject).
* A user should see his received friend requests in real-time (live) if he is online when
someone sends him a friend request.
* When a friend request is accepted, the two users become friends. Therefore, they will be
able to see each other’s status updates. Assume all status updates’ visibility is friends-
only; meaning only friends can see each others’ status posts (they are not public).
* Post Status: A user should be able to post status updates.
* See Timeline (Wall): A user should be able to see his timeline at any time, which is the
history of all of his past status update posts, in chronological order.
* See News Feed (Homepage): A user should be able to see his news feed, which is the last
ten status updates by his friends, in chronological order.

## Execution
This program has been created on top of a network topology created in a file called 'finalTopol.py'. The topology consists of three clients connected to two switches which in turn are connected to a server. The topology is shown in the picture below:
[[https://github.com/jthak002/fb-python/topol.png|alt=topologyIllustration]]
The mininet topology can be run within a mininet VM with an x-server(for rendering the gui) enabled. the command for running the topology is: 
```sudo mn --custom finalTopol.py --topo mytopo -x```
If the file runs successfully we see the following output:
[[https://github.com/jthak002/fb-python/topol-exec.png|alt=topologyExecution]]
Also, a number of console windows will open for each node in the topology i.e. one for the server, one for EACH client and so on.
[[https://github.com/jthak002/fb-python/topolWindow.png|alt=topologyWindows]]

## Application Setup and Execution 
open the 'src-server' directory in the host:s1 console window. execute the 'python server.py' file to start the execute the server side of the application.[[https://github.com/jthak002/fb-python/server-py.png|alt=serverWindow]] now switch to one of the three client windows and switch to 'src-client' directory and execute 'python client.py' to execute the client side of the facebook application. The client will ask for the username and password (for the purposes of the test the usernames and the passwords are the same and can be found in upass.txt). The login for the users can be found in the `upass.txt` file, and all the changes in the passwords will be reflected in that file. Once the correct credentials are entered, the user can login to the site and he/she will be presented with the menu of options.[[https://github.com/jthak002/fb-python/client-py.png|alt=clientWindow]] At this point of time we can see that the server windows `host:s1` logs the traffic from every client that tries to login, including the successful and failed login/logout attempts.
