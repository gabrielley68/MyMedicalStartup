# MyDigitalStartup medical web project
## Installation guide
### Clone the repository
Run command : `git clone https://github.com/gabrielley68/MyMedicalStartup.git`  
Move to newly created directory `cd MyMedicalStartup`  

### Download dependencies
If not installed, [install composer](https://getcomposer.org)  
Run `composer install` in the newly created directory

### Setup Vagrant & Homestead
Install [Vagrant](https://www.vagrantup.com/downloads.html) and [VirtualBox](https://www.virtualbox.org/wiki/Downloads)  
Download Homestead by running command `vagrant box add laravel/homestead` (might require to reload the terminal)  
Copy and edit the file Homestead.example.yaml into Homestead.yaml:  
 - Change 'C:\Path\To\MyMedicalStartup' to the absolute path of the project  

Run command `vagrant up` to launch the server and wait until the virtual machine is set  
Symfony app is now available at http://192.168.10.10   
(Please note that you need to start vagrant each time, possible in PHPStorm (Tools > Vagrant > Run))  
 
### (Optionnal) PhpMyAdmin
Download [PhpMyAdmin](https://www.phpmyadmin.net)  
Change 'C:\Path\To\PhpMyAdmin' to the absolute path of the PhpMyAdmin installation  
Run command `vagrant reload --provision`  
PhpMyAdmin is now available at http://192.168.10.10:8000  
Credentials are user: 'homestead' and password: 'secret'  
  
### (Optionnal) Set hostname for Windows
Edit hosts file with administrator rights (usual at `C:\Windows\System32\drivers\etc\`)  
Add the line `192.168.10.10 mymedicalstartup.fr` and save
You may now access to the project at the address http://mymedicalstartup.fr/ (and http://mymedicalstartup.fr:8000/ for PhpMyAdmin)
