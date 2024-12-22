# AWS PYTHON FLASK DOCKER

#### SSH Commands
* change permission of the `.pem` file
    ```bash
    chmod 0400 .pem file path
    ``` 
* connect to remote server using ssh
    ```bash
    ssh ec2-user@public_ip
    ```
    in case you choose `Ubuntu` os then
    ```bash
    ssh ubuntu@pubic_ip
    ```

#### Install Packages
* update the system
    ```bash
    sudo apt-get update
    ```
* install git
    ```bash
    sudo apt install git
    ```
* install docker
    ```bash
    sudo apt-get update
    sudo apt-get install ca-certificates curl
    sudo install -m 0755 -d /etc/apt/keyrings
    sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
    sudo chmod a+r /etc/apt/keyrings/docker.asc
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    sudo apt-get update
    sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    ```

* add docker to the user to use it without sudo
    ```bash
    sudo groupadd docker
    sudo usermod -aG docker $USER
    ```
- 1)  https://www.youtube.com/watch?v=bQP3f9iP2A0&list=LL&index=4
- 2) https://docs.docker.com/engine/install/ubuntu/


- sudo docker build -t youtube-demo .
- sudo docker images
- sudo docker run -p 5000:5000 youtube-demo
- sudo docker run -d -p 5000:5000 --restart unless-stopped  youtube-demo
- sudo docker stop 0656665b(whatever id you got)
sudo docker run -d -p 5000:5000 --restart unless-stopped  youtube-demo
sudo docker ps


how to change permissions:
go to security settings of .pem file and remove inheritance and also add only your main with read and execute permissions
