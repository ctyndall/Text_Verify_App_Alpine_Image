## Example application with mobile phone PIN verification
The tarball in this repository contains a docker image that contains:
	-Alpine Linux distribution
	-Python 2.7
	-GNU nano text editor
	-flask, twilio
	-app and config files

# Requires
    -docker
	-port 5000 on localhost available
	
## Instructions
1. Download/clone text_verify_app_docker_image
2. Navigate to the folder where you downloaded and load the image with docker using:
	 'docker load -i text_verify_app_alpine.tar'
3. Run the image using:
     'docker run -it -p 5000:5000 text_verify_app_alpine /bin/sh'
4. Once the image is loaded, edit the config.py file using nano:
	 'nano config.py'
5. Fill in your twilio account, token, and phone number and save the file.
6. Run app.py with python 2.7 using:
	 'python app.py'
7. Point your browser to "0.0.0.0:5000".
NOTE: If you are using DockerQuicktartTerminal/boot2docker, 
	  you may need to point to the IP listed upon loading the QuickStart terminal
	  instead of 0.0.0.0
