
# Pre-Requisites
  - Update and Refresh Repository Lists
    ```ssh
    $ sudo apt-get -y upgrade
    ```
    
  - Install Python 3.7
    ```ssh
    $ sudo apt-get install -y python3.7
    ```
    
  - Install pip for Python 3
    ```ssh
    $ sudo apt-get install -y python3-pip
    ```
    
  - Update python and pip alias
    Open `~/.bashrc` file
    ```ssh
    $ gedit ~/.bashrc
    ```
    Insert new alias
    ```ssh
    alias python=python3
    alias pip=pip3
    ```
    Add changes to cli
    ```ssh
    $ source ~/.bashrc
    ```
    Check versions
    ```ssh
    $ python -V
    Python 3.6.9
    $ pip -V
    pip 9.0.1 from /usr/lib/python3/dist-packages (python 3.6)
    ```
    
  - Install Docker
    ```ssh
    $ sudo apt-get remove docker docker-engine docker.io containerd runc
    $ sudo apt-get update -y
    $ sudo apt-get install \
        apt-transport-https \
        ca-certificates \
        curl \
        gnupg-agent \
        software-properties-common
    $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    $ sudo apt-key fingerprint 0EBFCD88
    $ sudo add-apt-repository \
        "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
        $(lsb_release -cs) \
        stable"
    $ sudo apt-get update
    $ sudo apt-get install docker-ce docker-ce-cli containerd.io -y
    $ apt-cache madison docker-ce
    $ sudo apt-get install docker-ce=<VERSION_STRING> docker-ce-cli=<VERSION_STRING> containerd.io
    $ sudo docker run hello-world
    ```
    
  - Install Docker Compose
    ```ssh
    $ sudo curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
    $ sudo chmod +x /usr/local/bin/docker-compose <- next code to run
    $ docker-compose --version
    ```
