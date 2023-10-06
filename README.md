## SETTING UP UBUNTU 20.04-LTS USING VAGRANT

**Step 1**  : Install a virtualization software.  
Here I want to use VirtualBox, of course you can use any other virtualization software to like.  
To download virtualbox go to: [virtualbox website](https://www.virtualbox.org/wiki/Downloads)
![](./images/1.png)

**Step 2**  
Create a new virtual computer on VirtualBox.  
Here, I can specify the name of the machine, operating system you want to install, RAM and hard disk size you want the computer to have.

**Step 3**  
I will create a directory where vagrant installation will be initialized from.

**Step 4**  
In the directory, do: `vagrant init ubuntu/focal64`  
This will create a Vagrantfile in the directory. Vagrantfile is a configuration file for vagrant where it get instructions on how to setup the Operating System.

Vagrant has a registry where it fetches operating system images for installation. 

**Step 5**  
Do: `vagrant up`  
This will install Ubuntu Operating System in the background, handling the user interaction processes that could have been performed if I was to install it from a CD or a bootable flash drive.  
It first checks the system if there is a sample of the virtual machine image for the Ubuntu version specified in the Vagrantfile (probably from a previous installation). if it can't find one on the machine, it then downloads the software from vagrant registry and installs it on the machine.

**Step 6**  
Do: `vagrant ssh`  
Installation is complete, and I can now login to my virtual machine from the terminal using the `vagrant ssh` command.

