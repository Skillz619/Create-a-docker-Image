# Create-a-docker-Image

We will build a docker Image and name it webapp-color

# Step -1 (goto the directory webapp-color)
$ cd /root/webapp-color/

# Step - 2 (Build the docker file with the tag webapp-color use the . to specify that you will run from this cmd from the directory)
$ docker build -t webapp-color . 

# Step - 3 (Run the image and publish on a port on the container to a port number on the host)
docker run -p 8282:8080 webapp-color
![image](https://github.com/Skillz619/Create-a-docker-Image/assets/43133388/0da5a269-c2b6-44a3-8740-26051b7f2e56)
It will start running on the port in the container


# Deploying a web app using docker
Deploy a web application named webapp using the kodekloud/simple-webapp-mysql image. Expose the port to 38080 on the host.

The application makes use of two environment variable:
1: DB_Host with the value mysql-db.
2: DB_Password with the value db_pass123.
Make sure to attach it to the newly created network called wp-mysql-network.


Also make sure to link the MySQL and the webapp container.

# Docker script to deploy the web app
docker run --network=wp-mysql-network -e DB_Host=mysql-db -e DB_Password=db_pass123 -p 38080:8080 --name webapp --link mysql-db:mysql-db -d kodekloud/simple-webapp-mysql

![image](https://github.com/Skillz619/Create-a-docker-Image/assets/43133388/4dd1d26d-e4c7-41d4-a3b0-ab9417d80de3)

