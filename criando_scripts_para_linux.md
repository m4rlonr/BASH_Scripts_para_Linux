Para criação de scripts no Linux é necessario alguns comando, aqui vamos criar scripts simples para distribuição Linux.
For creating of scripts on Linux is need some of commands, here let's creating simple for distribution Linux.

starting-------------------------------------------------------------------------------------------------------------

Open an editor of text
Create a file with format .sh
Example: script.sh
Open the file on editor

#!/bin/bash

#acess root to get permissions and execute the commands
sudo su

#go to initial path
cd

#update the repository
apt update

#upgrade the programs and libraries
apt upgrade

#after all the codes we will use this command
apt install -f

#Command to exit the prompt of command and user root
exit

Now let's instalating programs--------------------------------------------------------------------------------------

#for installing geany
apt install geany

#for installing codeblocks
apt install codeblocks

#for installing Sublime-Text
apt install snapd
sudo snap install sublime-text --classic --candidate

#for installing snap/snappy
apt install snapd

#for installing google chrome
sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
apt update
apt install google-chrome-stable

#for installing Opera mini
apt install snapd
snap install opera

#for installing spotify
apt install spotify-client

#for installing VLC
apt install vlc

#for installing VirtualBox/Virtual Machine
apt install virtualbox

#for installing WPS-Office
apt install snapd
snap install wps-office-all-lang-no-internet

#for installing NetBeans
apt install netbeans

#for installing Node.js
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
source ~/.profile
nvm ls-remote
nvm install 10.16.0
node --versio

#for installing vscode
sudo snap install --classic code

Now an example generic of script-----------------------------------------------------------------------------------

#!/bin/bash

sudo su
<enter the root password>
cd
apt update
apt upgrade
<command for installing the programs>
apt install -f 
exit
exit

Example the installing google chrome, geany and WPS-Office-------------------------------------------------------------

sudo su
<enter the root password>
cd
apt update
apt upgrade

sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
apt update
apt install google-chrome-stable

apt install geany

apt install snapd
snap install wps-office-all-lang-no-internet

apt install -f 
exit
exit

To run script ------------------------------------------------------------------------------------------------

#go to save file location
#right-click and open the command prompt in the folder where the file is saved
#immediately after entering the following command.

sudo chmod + x <name_file> .sh

#and to execute the script still with open terminal type

. / <name_file> .sh

