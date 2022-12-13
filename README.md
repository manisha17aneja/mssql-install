video link
=============

https://www.youtube.com/watch?v=t53-trtWziQ

commands from video
================

sudo apt update && sudo apt upgrade -y

clear

wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -

sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-preview.list)"

sudo apt update

clear

sudo apt install mssql-server -y

sudo /opt/mssql/bin/mssql-conf setup

sudo systemctl status mssql-server

curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -


curl https://packages.microsoft.com/config/ubuntu/20.04/prod.list | sudo tee /etc/apt/sources.list.d/msprod.list''

sudo apt update

sudo apt install mssql-tools unixodbc-dev

echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bash_profile

echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bashrc

source ~/.bashrc

TO CHECK MSSQL VERSION

sqlcmd -S localhost -U SA -Q 'select @@VERSION'

sudo ufw status

sudo ufw enable

sudo ufw allow 1433

sudo ufw allow 1434

sudo ufw reload

sudo ufw status

extra
================

sudo apt-get install -y libodbc1

sudo apt update

sudo apt install unixodbc


extra
================
curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -

echo "deb [arch=amd64] https://packages.microsoft.com/ubuntu/20.04/prod bionic main" | sudo tee /etc/apt/sources.list.d/mssql-release.list

sudo apt update

sudo apt install msodbcsql17
