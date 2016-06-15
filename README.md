# windows_elasticsearch

A virtual machine that installs elasticsearch to sandbox and test locally

Dependencies
	VirtualBox 
	https://www.virtualbox.org/wiki/Downloads

	Vagrant 
	https://www.vagrantup.com/downloads.html

Once cloned, run a shell into the location and run the command:
	vagrant up

This does the following
	-installs java, ansible, git, and curl which are pre-requisites
	-installs elasticsearch
	-installs mobz elasticsearch-head to visualize the elasticsearch cluster

Once the machine is running, ssh in with the command
	vagrant ssh

To add data to elastic, copy and paste a few lines from the favorites_insert.txt file provided

To see a visualization of the data, open this url in a browser
	- http://localhost:9200/_plugin/head/

To have a simple query interface to the cluster install the chrome plugin Sense (available in Chrome Store)

Where to go from here?
	It is possible to halt or suspend the vm although I usually keep the cluster on all times
	When getting rid of the cluster I run the command vagrant destroy which takes care of all the cleanup