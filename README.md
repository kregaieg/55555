# Prerequisites
## Install Docker
#### For Windows
Install [Docker Toolbox.](http://docs.docker.oeynet.com/toolbox/toolbox_install_windows/)
#### For Linux
Follow the steps below to install Docker on Linux from Latest Docker’s Repository.  
Update the system and install required dependencies typing following command:  
**sudo yum update && sudo yum install yum-utils device-mapper-persistent-data lvm2**  
Next, add the repository to your system typing following in the terminal:  
**sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo**  
Install Docker Community Version typing following command:  
**sudo yum install docker-ce**  
Start and Enable Docker service typing following systemctl commands:   
**sudo systemctl start docker**   
**sudo systemctl enable docker**   
You can check the Docker service status using the following systemctl command:   
**sudo systemctl status docker**
## Install Docker Compose For Linux

Install Extra Packages for Enterprise Linux:   
**sudo yum install epel-release**  
Install python-pip:  
**sudo yum install -y python-pip**  
Then install Docker Compose:  
**sudo pip install docker-compose**
# Build Image
Build the new image using the command **docker build -t automation-template-jenkins-docker "path"**. Path refers to the directory containing the Dockerfile.  
At the end of the process you should see the message **Successfully built "image ID"**.
# Start Image
Run the new image on port 8080 using the command **nohup docker-compose up &**  
If you’re using Docker natively on Linux, then the image should now be listening on port 8080 on your Docker daemon host. Point your web browser to http://IP-ADDRESS:8080.  
If you’re using Docker Machine on Windows, use docker-machine ip MACHINE_VM to get the IP address of your Docker host. Then, open http://MACHINE_VM_IP:8080 in a browser.
