# Nitc-auth-CLI


![MIT License](https://img.shields.io/github/license/AmarNathH/nitc-auth-cli.svg?label=License)

These scripts can be used for logging in and out of NITC Network from the CLI itself, without any need for GUI. It has been made sure that the script uses only bare-minimum external programs which is commonly available in any minimal Linux-based systems, so that it can be used in various headless systems such as Servers, Raspberry-pi..etc.

| File | Description |
|------|:------|
| `login.sh` | This script will prompt the user for username and password, and will give appropriate status feedback for logging into the network. |
| `logout.sh` | This script is responsible for logging you out, it will logout from the network and give appropriate feedback for logout. It is highly recommended to use this script with the login script only. |
| `log_file` | This file will be generated by `login.sh`. This file stores the information about current session's key as well as the details of the network, this is used by the logout script.|

**Dependencies:** wget, curl, sed  
Make sure you have the dependencies before using the script, if you don't have the dependencies then use the following command to install them  
`$ sudo apt install wget curl sed`


### Usage Guidelines
**Without Installation (recommended)**    
First go to the directory containing the files.  
`$ cd path/to/nitc-auth-cli/directory`  
Then open the terminal in the current directory and use the following command to login and enter the details as prompted.  
`$ ./login.sh`  
To Logout from the current session use the command  
`$ ./logout.sh`

**After Installating**  
For installing you have to execute the following command,  
`$ sudo ./install.sh`   
During installation the files will be copied to `/opt/nitc-auth-cli` and some alias commands will be added to your `.bashrc` or `.zshrc`.  
Now you can open your terminal and use the commands `nitc-login` for logging in, `nitc-logout` for logging out and `nitc-logfile` for viewing the contents of your `log_file` 

### Troubleshooting  
If you are not able run the scripts, you can use the command  
`chmod +x <script-name>.sh`  
This will change the permission of the script files, and will allow you to run the scripts
