## Install NVM

NVM is a command-line utility to install and manage Node.js versions for specific users. You can install nvm using a shell script provided by the nvm team.

1. First, make sure you have curl installed on your system

    ```sh
    sudo apt update && sudo apt install curl -y
    ```
    
 2. Next, run the following command to configure nvm on your system for current logged user.

    ```sh
    curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash 
    ```
  
 3. Reload system environment using this command. It will set the required environment variables to use nvm on the system.
    ```sh
    source ~/.profile 
    ```
    ```sh
    source ~/.bashrc
    ```
    
 4. Find available Node JS version.

    ```sh
    nvm ls-remote 
    ```
    
 5. Now install the node.js version you need to use for running the node.js application. Below command will install node.js 14.15.0 the LTS release on your system.

    ```sh
    nvm install v14.15.0
    ```
    
