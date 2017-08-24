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

