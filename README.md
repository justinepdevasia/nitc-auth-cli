# Nitc-auth-CLI


![platform-Linux](https://img.shields.io/badge/platform-Linux-orange.svg) [![made-with-bash](https://img.shields.io/badge/Made%20with-Bash-1f425f.svg)](https://www.gnu.org/software/bash/) [![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html)

These scripts can be used for logging in and loggin out from NITC Network in the CLI itself, without any need for GUI. These can be used in headless systems such as Servers, Raspberry-pi..etc. It has been made sure that the script uses only bare-minimum external programs which is commonly available in any minimal Linux-based systems.

| File | Description |
|------|:------|
| `login.sh` | This script will prompt the user for username and password, and will give appropriate status feedback for logging into the network. |
| `logout.sh` | This script is responsible for logging you out, it will logout from the network and give appropriate feedback for logout. |
| `log_file` | This file will be generated by login.sh. This file stores the information about current session's key as well as the details of the network, this is used by the logout script.|

You can install the files to your system by using the `install.sh` script. The installation will install the files to the `/opt/nitc-auth-cli` directory and will add aliases for the `login.sh`,`logout.sh` and `log_file`. You can then execute the login script by using the command `nitc-login`, logout script by using the command `nitc-logout` and you can see the content inside `log_file` with the command `nitc-logfile`.  As of now the install.sh script supports bash and zsh shells.

 If you are not able run the scripts, you can use the command
 
`chmod +x <script-name>.sh`

This will change the permission of the script files, and will allow you to run the scripts
