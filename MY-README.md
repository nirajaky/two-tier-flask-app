## Deployment with docker(2)
1. Create a EC2 instance on aws
2. Connect your EC2 intance with local machine using SSH client
3. Install docker on the EC2 instance
    > sudo apt update
    > sudo apt install docker.io
4. git clone the flask repo
5. Write Dockerfile
6. docker build . -t flaskapp
    - . -> path where Dockerfile is located
    - -t flaskapp -> name of the image(-t tag)
    - docker images
7. docker run -d -p 5000:5000 flaskapp:latest
    - -d = detached mode, -p = port forwarding  
    - above command runs the image flaskapp and creates the container
    - docker ps
8. By default the servers inbound to port 5000 is disabled
    - We need to go security group of instance and edit inbound rule and add Custum TCP with 5000 port, Source - Anywhere

Hello




