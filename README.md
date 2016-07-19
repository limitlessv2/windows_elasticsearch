# windows_elasticsearch

A virtual machine that installs elasticsearch to sandbox and test locally

Dependencies
	
	VirtualBox 
	https://www.virtualbox.org/wiki/Downloads

	Vagrant 
	https://www.vagrantup.com/downloads.html

	Git shell (preferred) 
	https://git-scm.com/download/win

	with the bottom option clicked for altering Path variable
	http://blog.osteel.me/posts/2015/01/25/how-to-use-vagrant-on-windows.html

Once cloned, run a shell into the location and run the command:
	
	vagrant up

If getting errors with setting hostname
	
	delete this line from the Vagrant file
	https://github.com/porivas/windows_elasticsearch/blob/master/Vagrantfile#L17

This does the following
	
	-installs java, ansible, git, and curl which are pre-requisites
	-installs elasticsearch
	-installs mobz elasticsearch-head to visualize the elasticsearch cluster

Once the machine is running, ssh in with the command
	
	vagrant ssh

If prompted for a passphrase and later a password

	press enter for the passphrase
	and "vagrant" for the password

To add data to elastic, copy and paste a few lines from the favorites_insert.txt file provided

To see a visualization of the data, open this url in a browser
	
	- http://localhost:9200/_plugin/head/

To have a simple query interface to the cluster install the chrome plugin Sense (available in Chrome Store)

Where to go from here?
	
	It is possible to halt or suspend the vm although I usually keep the cluster on all times
	When getting rid of the cluster I run the command 
		vagrant destroy 
	which takes care of all the cleanup