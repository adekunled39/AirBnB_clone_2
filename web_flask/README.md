0x04. AirBnB clone - Web framework
Python
Back-end
Webserver
Flask
 By: Guillaume, CTO at Holberton School
 Weight: 2
 Project will start Nov 10, 2022 6:00 AM, must end by Nov 14, 2022 6:00 AM
 was released at Nov 11, 2022 6:00 AM
 Manual QA review must be done (request it when you are done with the project)
 An auto review will be launched at the deadline
Concepts
For this project, we expect you to look at this concept:

AirBnB clone
Resources
Read or watch:

What is a Web Framework?
A Minimal Application
Routing (except “HTTP Methods”)
Rendering Templates
Synopsis
Variables
Comments
Whitespace Control
List of Control Structures (read up to “Call”)
Flask
Jinja
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

General
What is a Web Framework
How to build a web framework with Flask
How to define routes in Flask
What is a route
How to handle variables in a route
What is a template
How to create a HTML response in Flask by using a template
How to create a dynamic template (loops, conditions…)
How to display in HTML data from a MySQL database
Copyright - Plagiarism
You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
You are not allowed to publish any content of this project.
Any form of plagiarism is strictly forbidden and will result in removal from the program.
Requirements
Python Scripts
Allowed editors: vi, vim, emacs
All your files will be interpreted/compiled on Ubuntu 14.04 LTS using python3 (version 3.4.3)
All your files should end with a new line
The first line of all your files should be exactly #!/usr/bin/python3
A README.md file, at the root of the folder of the project, is mandatory
Your code should use the PEP 8 style (version 1.7)
All your files must be executable
The length of your files will be tested using wc
All your modules should have documentation (python3 -c 'print(__import__("my_module").__doc__)')
All your classes should have documentation (python3 -c 'print(__import__("my_module").MyClass.__doc__)')
All your functions (inside and outside a class) should have documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)')
A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)
HTML/CSS Files
Allowed editors: vi, vim, emacs
All your files should end with a new line
A README.md file at the root of the folder of the project is mandatory
Your code should be W3C compliant and validate with W3C-Validator (except for jinja template)
All your CSS files should be in the styles folder
All your images should be in the images folder
You are not allowed to use !important or id (#... in the CSS file)
All tags must be in uppercase
Current screenshots have been done on Chrome 56.0.2924.87.
No cross browsers
More Info
Install Flask
$ pip3 install Flask



Manual QA Review
It is your responsibility to request a review for this project from a peer before the project’s deadline. If no peers have been reviewed, you should request a review from a TA or staff member.

Tasks
0. Hello Flask!
mandatory
Write a script that starts a Flask web application:

Your web application must be listening on 0.0.0.0, port 5000
Routes:
/: display “Hello HBNB!”
You must use the option strict_slashes=False in your route definition
guillaume@ubuntu:~/AirBnB_v2$ python3 -m web_flask.0-hello_route
* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....
In another tab:

guillaume@ubuntu:~$ curl 0.0.0.0:5000 ; echo "" | cat -e
Hello HBNB!$
guillaume@ubuntu:~$ 
Repo:

GitHub repository: AirBnB_clone_v2
Directory: web_flask
File: 0-hello_route.py, __init__.py
   
1. HBNB
mandatory
Write a script that starts a Flask web application:

Your web application must be listening on 0.0.0.0, port 5000
Routes:
/: display “Hello HBNB!”
/hbnb: display “HBNB”
You must use the option strict_slashes=False in your route definition
guillaume@ubuntu:~/AirBnB_v2$ python3 -m web_flask.1-hbnb_route
* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....
In another tab:

guillaume@ubuntu:~$ curl 0.0.0.0:5000/hbnb ; echo "" | cat -e
HBNB$
guillaume@ubuntu:~$ 
Repo:

GitHub repository: AirBnB_clone_v2
Directory: web_flask
File: 1-hbnb_route.py
   
2. C is fun!
mandatory
Write a script that starts a Flask web application:

Your web application must be listening on 0.0.0.0, port 5000
Routes:
/: display “Hello HBNB!”
/hbnb: display “HBNB”
/c/<text>: display “C ” followed by the value of the text variable (replace underscore _ symbols with a space )
You must use the option strict_slashes=False in your route definition
guillaume@ubuntu:~/AirBnB_v2$ python3 -m web_flask.2-c_route
* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....
In another tab:

guillaume@ubuntu:~$ curl 0.0.0.0:5000/c/is_fun ; echo "" | cat -e
C is fun$
guillaume@ubuntu:~$ curl 0.0.0.0:5000/c/cool ; echo "" | cat -e
C cool$
guillaume@ubuntu:~$ curl 0.0.0.0:5000/c
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<title>404 Not Found</title>
<h1>Not Found</h1>
<p>The requested URL was not found on the server.  If you entered the URL manually please check your spelling and try again.</p>
guillaume@ubuntu:~$ 
