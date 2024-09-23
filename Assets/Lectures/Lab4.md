# 20CYS402 - Distributed Systems and Cloud Computing
![](https://img.shields.io/badge/Batch-21CYS-lightgreen) ![](https://img.shields.io/badge/UG-blue) ![](https://img.shields.io/badge/Subject-DSCC-blue) <br/>
![](https://img.shields.io/badge/Lecture-2-orange) ![](https://img.shields.io/badge/Practical-3-orange) ![](https://img.shields.io/badge/Credits-3-orange) <br/>

## Docker
![](https://img.shields.io/badge/Date-23_September-blue)

## Objective
To understand:
  - Docker and Docker Hub
  - Create Docker image and build
  - Upload the built docker image to Docker Hub

### Examples
- [Simple Dockerfile Building](https://www.youtube.com/watch?v=0HCBQpfQE7o)
- [Demo Dockerfile Building](https://www.youtube.com/watch?v=lrTBwlW46Ik)
- [Demo Image Running](https://www.youtube.com/watch?v=ND-qkZVc3KM)
- [Pushing Image to DockerHub](https://www.youtube.com/watch?v=pBdN1OlWGQc)

### Class Practice - 1

```
docker run hello-world
```

<p align="center">
  <img src="../images/docker_hello-world.png" width=800/>
</p>

### Class Practice - 2

```
docker pull nginx
```

<p align="center">
  <img src="../images/docker_nginx.png" width=800/>
</p>

```
docker run -d -p 8080:80 nginx
```

### Class Practice - 3

- The base layer is "alpine"
- Set a Environmental Variable called "ROLLNO" to your full roll number (CB.EN.U4CYS210YY)
- Make a directory called "20CYS402"
- Change Directory to "20CYS402"
- Create a file called "Assignment.txt" and write your DockerHub username to it

### Assignment: Create a Docker Image for a Database Connector

####  Objective:
Build a Docker image for a database connector application. The application connects to a database using a specific programming language and requires the installation of certain packages. Set environment variables for database connection details and expose the application on a specific IP address and port.

#### Requirements:
 - Choose a base image appropriate for the chosen programming language (e.g., Python, Node.js, Ruby).
 - Install the necessary packages for connecting to a database. Choose a simple database connector library compatible with your chosen language (e.g., psycopg2 for Python, mysql2 for Node.js, pg for Ruby).
 - Set environment variables for the following database connection details:
   - Database host
   - Database port
   - Database username
   - Database password
   - Database name
 - Expose the application on a specific IP address and port (e.g., IP: 0.0.0.0, Port: 8080).
 - Create a sample application code that uses the installed database connector library to connect to a database (you can use dummy values for the connection).

#### Tips:
 - Use an official base image related to the chosen programming language.
 - Clearly document each step in the Dockerfile using comments.
 - Make sure to expose the correct port for your application.
 - Test the Docker image locally to ensure the database connector application is running.

#### Submission:
Provide the following in your submission:
 - The Dockerfile used to build the Docker image.
 - The source code of the sample application demonstrating the database connection.
 - Link to Image in Docker Hub.

#### DockerHub User ID and Assignment Submission Status


  
