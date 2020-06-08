This app uses:
1. Node and NPM 
2. Ionic Cli
3. AWS RDS - PostgreSQL instance, Postbird tool, and an S3 bucket
4. Docker Desktop 

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
1. Build the images: `docker-compose -f ./udacity-c3-deployment/docker/docker-compose-build.yaml --parallel`
2. Push the images: `docker-compose -f docker-compose-build.yaml push` //optional
3. Run the container: `docker-compose up`

#### Add Kubernetes config for our application
 ```bash 
    cd udacity-c3-deployment/k8s
 ```
1. Apply all files to cluster with your data: `kubectl apply -f {file} `


### Notes
Most of code came from [Udacity project](https://github.com/udacity/nd9990-c3-microservices-v1/tree/master/lesson-3-Container/solution/)
