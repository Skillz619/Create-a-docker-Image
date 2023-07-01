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
