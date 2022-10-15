# Dockerreact

This is the simple boiler plate react app which is further dockerized.

Link to the image on dockerhub: https://hub.docker.com/r/tandan/dockerreact

The two important files for creating build version are in **Dockerfile, nginx.conf**

After having these files following command has to be executed to create a docker image:

        npm run build
        
        docker build --tag dockerreact:1.0.0 .

Follow the following commands to run the container on your device:

- This command will pull the image from dockerhub in your system
    
      docker pull tandan/dockerreact:1.0.0
   
- This command will create a container for the image 

      docker run -d tandan/dockerreact:1.0.0
    
- After running this command details regarding this container will be displayed, what we need is port number here to map the system's port number to the port number which will appear now

      docker ps
    
- After getting port number(80 in this app) run following command to create another container on port number 4444

      docker run -d -p 4444:80 tandan/dockerreact:1.0.0
    
- After successfully running above command, open *http://localhost:4444/* on your browser, and the basic boiler plate code will be infront of you
