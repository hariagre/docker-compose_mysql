Now we have to create a yaml file with creating an image code into it as below:
vi docker-compose.yaml

and then give the below command to run and install as per docker-compose yaml.
docker-compose up -d

here pass the -d flag (for “detached” mode) used when we want to run services in background.
The output will be as below:

 

To stop your services: To stop the running services, use the following command:

docker-compose down
For this we need to delete the space i.e., we need to delete all the containers with below one command:
docker rm $(docker ps -a -q)

a-> stands of all containers and q-> stands for quit

For to delete all the images below one command we can use:

docker rmi $(docker images -q)

Then again run below command to run and install as per docker-compose yaml.

docker-compose up -d

installation is done with below screenshots:

 

Now need to add some ports like 8081 in security group of generated EC2 instance as below:

 

Then now copy the public IP address of the instance and add 8081 in the last and paste in browser with 8081 in the last as shows below:
 

Then login into it with below credentials:

Server field should keep blank

Username: db_user
Password: db_user_pass
