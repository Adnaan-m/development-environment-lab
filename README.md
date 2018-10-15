# Development-Environment-Lab

## Description
The following ReadMe displays information relating to the task set to use Vagrant.

## Task One
The first task was to ensure that there was a platform on to which you could use your virtual machine, this was called VirtualBox. Think of this as an 'inception' application providing a machine within a machine in order to use specific platforms... in this case it was Ubuntu.

## Task Two
Task two was introducting the storage of files in order to make this happen, this was through using Vagrant, in more detail th Vagrant file.

## Task Three 
### Commands 
The following task involves the commands used to do specific tasks within the environment, an explanation will follow.

```
(Terminal)
vagrant init ubuntu/ <filename>
```
This command initiaises the current directory to be a vagrant environment.

```
(Terminal)
vagrant up
```
This creates and configures the machine.

```
(Terminal)
vagrant ssh
```

This goes into the the vagrant machine.

```
(Terminal)
sudo apt-get update && upgrade -y
```
The following code updates and installs the most up-to-date files from the Vagrant File onto the achine. NOTE! This is important to do to ensure that the machine does not break during a project.

```
(Terminal)
sudo apt-get install nginx -y
```
The following code provides access to the server.

```
(Terminal)
curl <http://localhost> 
```
The following code accesses the website through curl.

## Task Four
Inside the vagrant file, a network file was established from which a private network was created with a specific IP address. The code is shown below. 

```rb
  config.vm.network "private_network", ip: "192.168.10.100"
```

Once the file is amended and saved, the system will need to initialise and re-read the file. In order to do this, if in the ssh file, first exit the workspace then reload the vagrant file within BASH. This is done by;

```
(Terminal)
exit
vagrant reload
```
If not in the workspace, exit would not need to be inputted.

