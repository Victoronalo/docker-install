# docker-install

Project: Introduction to Docker



-I created an EC2 instance named docker-instance



-I also created a key pair  named docker-keys


-I configured the security group



-First of all I ran the command sudo apt-get update to get update on Ubuntu




-To install certificates and other installations I ran the command
             *sudo apt-get install ca-certificates curl gnupg




-To create a directory and withspecific permission (0755) I ran the command
             *sudo install -m 0755 -d /etc/apt/keyrings



-To download Docker GPG key using curl I ran the command
           *curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o        /etc/apt/keyrings/docker.gpg



-I set read permission for all user on Docker GPG by running
         *sudo chmod a+r /etc/apt/keyrings/docker.gpg




-I created a Docker APT repository by running the below command
       *echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null





-To get latest version of docker I ran this command sudo apt-get update




-To verify installation of docker has been successful I used the command
         *sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin




-To check the status I used this command *sudo systemctl status docker




-I used this “sudo usermod -aG docker Ubuntu” not to use sudo in feature




-I then ran the command “docker run hello-world”



-It was successful



-This project has given me introduction to docker as a container and how to go around it.

