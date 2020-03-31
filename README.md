We have already described the instructions at `https://github.com/udacity/nd9990-c3-microservices-v1/blob/master/lesson-2-Independent-Development/exercises/README.md` to get the following installed on your system.
1. Node and NPM 
2. Ionic Cli
3. AWS RDS - PostgreSQL instance, Postbird tool, and an S3 bucket
4. Docker Desktop  - [macOS](https://docs.docker.com/docker-for-mac/install/), [Windows 10 64-bit: Pro, Enterprise, or Education](https://docs.docker.com/docker-for-windows/install/), [Windows  10 64-bit Home](https://docs.docker.com/toolbox/toolbox_install_windows/). You can find installation instructions for other operating systems at:  https://docs.docker.com/install/

### Instructions
The project is composed by the following sub folders:
1. udacity-c3-frontend - For Ionic client web application, which consumes the RestAPI Backend
2. udacity-c3-restapi-feed - For "feed" microservice
3. udacity-c3-restapi-user - For "user" microservice
4. udacity-c3-deployment/docker - For running the Nginx as a reverse-proxy server
5. for each with package.json you should install dependencies
 ```bash 
    cd folder
    npm install
 ```

#### Create Docker Images for our application
* Create a Dockerfile for all the **three** services in the respective directories. The three services are - "feed", "user", and "frontend". 
* Use the Dockerfile to create the corresponding images for all the **three** services.
* ``` each_folder/docker build . ```

#### Task 4 - Create and Run the containers for all the Images
*   Use `docker run` to create and run the image as container. Do this for all the services and reverse proxy.

#### Task 5 - Docker compose
*   Use docker-compose to deploy the completed application 

Bonus: Use `docker compose` to build our images. 

### Notes
Most of code came from [Udacity project](https://github.com/udacity/nd9990-c3-microservices-v1/tree/master/lesson-3-Container/solution/)
