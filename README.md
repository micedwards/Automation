# Network Programmability & Automation 
2016.12.19 - Light the New World

This was put together as a form of tracking my path through the network automation jungle.  
The choice of tools to learn is mostly environment based and as most of the customers I work for are Cisco based with a mix of firewalls/loadbalancers I am personally working through Python + netmiko & ciscoconfigparse for simple stuff and will be adding Ansible or Salt to the mix. I am using Cisco's VIRL as my test network.   
VIRL has an API too, it would be nice to able to completely automate the build and configuration of the VIRL test environment...

Originally started as an URL dump and as a GIT practice project. Most comments are cribbed from the source site or 
  https://en.wikipedia.org/wiki/Comparison_of_open-source_configuration_management_software

## Linux Cheat Sheet:
  https://fosswire.com/post/2007/08/unixlinux-command-cheat-sheet/

## GIT
Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed & efficiency. [Oh that sounds so cute... but it is hard to get your head wrapped around how git works]
* https://git-scm.com/downloads
* http://rogerdudler.github.io/git-guide
* https://git-scm.com/book/en/v2
* https://www.codeschool.com/ Codeschool has a free introduction GIT lesson (learn by doing)

## Network programming blogs:
* https://jedelman.com/           @jedelman8 [http://networktocode.com/]
* https://pynet.twb-tech.com/     @kirkbyers [netmiko]  
* https://networklore.com/        Patrick Ogenstad
* http://keepingitclassless.net/  @mierden  [ToDD]
* https://sreeninet.wordpress.com 
* https://codingnetworker.com    Henry Ölsner 
* http://packetlife.net    Jeremy Stretch [NetBox]

## Cisco Network Programmability and DevOps Learning Map - Foundations
https://communities.cisco.com/docs/DOC-66387 links out to training sites some of which are free (including [CodeSchool](https://www.codeschool.com/))


## LANGUAGES:

Seven part [getting started with coding](http://vegaskid.net/2016/12/getting-started-with-coding-part-1-introduction/)


### Python
Search the O'Reilly website for the free eBooks "A Whirlwind Tour of Python" & "How to Make Mistakes in Python" (worth reading the first chapter or so of Mistakes before installing any version of Python) 
* https://www.python.org
* https://www.continuum.io/downloads Anaconda: Python + development environment (I use this)
* https://developers.google.com/edu/python is the website of Google’s (free) Python course
* https://www.codeschool.com/ Codeschool has a free introduction Python lesson
* https://training.talkpython.fm also home to a good python podcast
* http://nedbatchelder.com/text PyCon talks good! 
* https://pythonprogramming.net/introduction-to-python-programming
* https://pythonprogramming.net/introduction-intermediate-python-tutorial

####     PEP8
Formatting standard for Python - nice except for 80 char line lengths... forget it I'll try keep them under 100 instead.

####     Six: Python 2 and 3 Compatibility Library
https://pythonhosted.org/six/

####     Netmiko
An open-source Python library that simplifies SSH management to network devices. The library is based on the Paramiko SSH library. 
* https://pynet.twb-tech.com/
* [Packet Pushers #270 Automation with Python & Netmiko](http://packetpushers.net/podcast/podcasts/show-270-design-build-9-automation-python-netmiko/)
    
####     ciscoconfparse 
ciscoconfparse is a Python library, which parses through Cisco IOS-style configurations
* http://www.pennington.net/py/ciscoconfparse  
* https://codingnetworker.com/2016/06/parse-cisco-ios-configuration-ciscoconfparse  
  I used this to dismantle ACE20 loadbalancer configurations into individual farms (with a little manual checking afterwards)

####     TextFSM
TextFSM is a Python module that implements a template based state machine for parsing semi-formatted text. Originally developed to allow programmatic access to information given by the output of CLI driven devices, such as network routers and switches, it can however be used for any such textual output.
https://github.com/google/textfsm/wiki/TextFSM
https://github.com/google/textfsm
http://www.oznetnerd.com/category/automation/textfsm/
https://codingnetworker.com/2015/08/parse-cli-outputs-textfsm/

####     pip installs: netaddr & ipaddress 
* https://netaddr.readthedoc.io/
* https://docs.python.org/dev/library/ipaddress.html

####     Trigger
Trigger is a Python framework and suite of tools for interfacing with network devices and managing network configuration and security policy. (similar to netmiko/paramiko? haven't looked deep at this yet)
* https://trigger.readthedocs.io/en/latest/overview.html

### Cisco DevNet - Network Programmability for Network Engineers
Training modules on programming REST APIs, NETCONF, RESTCONF and APIC-EM APIs.
https://learninglabs.cisco.com/tracks/netprog-eng 

### YAML: YAML Ain't Markup Language
YAML is a human friendly data serialization standard for all programming languages.
* http://yaml.org/
* http://docs.ansible.com/ansible/YAMLSyntax.html
* http://www.yaml.org/spec/1.2/spec.html

### JSON 
(JavaScript Object Notation) is a lightweight data-interchange format. 
* http://json.org/

### JINJA2 
Jinja2 is a full featured template engine for Python.
* http://jinja.pocoo.org

### RUBY (Useful for Chef)
* http://www.ruby-lang.org/en/
* http://ruby-doc.org/
* https://en.wikipedia.org/wiki/Why%27s_(poignant)_Guide_to_Ruby


## Open-source Configuration Management Software
* https://en.wikipedia.org/wiki/Comparison_of_open-source_configuration_management_software
  
Good podcasts on these topics on Packet Pushers: 
* http://packetpushers.net/podcast/podcasts/show-176-intro-to-python-automation-for-network-engineers
* http://packetpushers.net/podcast/podcasts/show-198-kirk-byers-network-automation-python-ansible
* http://packetpushers.net/podcast/podcasts/show-270-design-build-9-automation-python-netmiko
* http://packetpushers.net/podcast/podcasts/datanauts-034-automate-packets
* http://packetpushers.net/podcast/podcasts/pq-show-99-netmiko-napalm-network-automation


Chef & Puppet are the older tools 

### CHEF
Chef is a configuration management tool written in Ruby, and uses a pure Ruby DSL for writing configuration "recipes". These recipes contain resources that should be put into the declared state. Chef can be used as a client–server tool, or used in "solo" mode
* https://www.chef.io/
* https://learn.chef.io/
* https://github.com/chef/chef
    
### PUPPET
Puppet consists of a custom declarative language to describe system configuration, distributed using the client–server paradigm, and a library to realize the configuration. The resource abstraction layer enables administrators to describe the configuration in high-level terms, such as users, services and packages. Puppet will then ensure the server's state matches the description. 
* https://puppet.com/
* https://puppet.com/resources/ebook/tools-for-learning-puppet
* https://github.com/puppetlabs

LEARNING LAB: 
* https://puppet.com/download-learning-vm  


One engineers view of Salt & Ansible, useful for an overview of both:
* http://jensrantil.github.io/salt-vs-ansible.html

### ANSIBLE
Combines multi-node deployment, ad-hoc task execution, and configuration management in one package. Manages nodes over SSH and requires python (2.4 or later) to be installed on them. Modules work over JSON and standard output and can be written in any language. Uses YAML to express reusable descriptions of systems.
* https://www.ansible.com/
* https://www.ansible.com/quick-start-video
* https://www.ansible.com/network-automation
* http://docs.ansible.com/ansible/index.html
* https://github.com/ansible/ansible
* https://networklore.com/ansible-getting-started/
* http://jpmens.net/2012/06/06/configuration-management-with-ansible/
* https://galaxy.ansible.com/Juniper/junos/
* http://docs.ansible.com/ansible/intro_networking.html
* http://docs.ansible.com/ansible/ios_config_module.html

LEARNING LAB:
* https://www.turnkeylinux.org/ansible **Ansible on a VM**
* https://github.com/turnkeylinux-apps/ansible/blob/master/docs/usage.rst

### SALT
Salt started out as a tool for remote server management. As its usage has grown, it has gained a number of extended features, including a more comprehensive mechanism for host configuration. This is a relatively new feature facilitated through the Salt States component. With the traction that Salt has gotten in the last bit, the support for more features and platforms might continue to grow.
* https://saltstack.com/community/ <-best starting point
* https://blog.talpor.com/2014/07/saltstack-beginners-tutorial/

LEARNING LAB: 
**uses Vagrant on Virtual Box to setup the lab ie automation in action**
* https://docs.saltstack.com/en/getstarted/fundamentals/index.html 

### StackStorm - Event-Driven Automation
StackStorm is a powerful open-source automation platform that wires together all of your apps, services and workflows. 
* https://stackstorm.com
* https://docs.stackstorm.com/overview.html
* https://keepingitclassless.net/2016/12/introduction-to-stackstorm
* https://github.com/StackStorm/st2

#### StackStorm Exchange
Automate all the things you already know and use
with dozens of ready-made integration packs.
Cloud providers, monitoring services, lightbulbs.
* https://exchange.stackstorm.org
#### ST2Vagrant
Deploy StackStorm event-driven automation platform locally with Vagrant  https://www.stackstorm.com
* https://github.com/stackstorm/st2vagrant

##Mixed stuffs:

### RBFS (REST based file-server)
RBFS provides a RESTful, JSON based, interface to a file system.
Highlights:
* Confirm file integrity with MD5 checking.
* Store user defined meta-data along with the files.
* Tracks file change and MD5 history
* Automatically builds necessary directory structure.
* HTTP basic authentication support.
* IP whitelisting or blacklisting.
* Store and retrieve the history of file changes.
* File vs. directory action detection.
* Automatic mimetype header setting based on extention.
* SSL support
* Records source IP and DNS name.
* https://github.com/cidrblock/RBFS

### VAGRANT
Vagrant is computer software that creates and configures virtual development environments. It can be seen as a higher-level wrapper around virtualization software such as VirtualBox, VMware, KVM and Linux Containers (LXC), and around configuration management software such as Ansible, Chef, Salt, and Puppet.
* https://www.vagrantup.com/
* http://www.vagrantbox.es/
* http://www.cyberciti.biz/cloud-computing/use-vagrant-to-create-small-virtual-lab-on-linux-osx

### VirtualBox
Free equiv to VMware Workstation Pro and you can create desktop shortcuts to start VMs directly
* https://www.virtualbox.org/wiki/Downloads
* https://www.virtualbox.org/manual/ch06.html

How to hook your VMware Workstation VM and Virtual Box VM together (to manage VIRL devices etc)
* http://www.sysprobs.com/setup-network-virtualbox-vmware-virtual-machines

### VMware stuff:
* https://rednectar.net/2011/07/20/vmware-interfaces-tutorial/
* http://www.virtualizationadmin.com/articles-tutorials/vmware-server-workstation-player-articles/understanding-virtual-networking-vmware-workstation-9.html
     
### Turnkey Linux 
VMs/ISOs/containers for various purposes:
* https://www.turnkeylinux.org/
* https://www.turnkeylinux.org/core  
* https://www.turnkeylinux.org/ansible

## ToDD
A highly extensible framework for distributed capacity and connectivity testing (Testing on Demand....Distributed!) 
* https://github.com/toddproject/todd
* https://www.youtube.com/watch?v=ZIykHS5RoNM
* http://packetpushers.net/podcast/podcasts/pq-show-81-network-testing-todd

## Nelkit (Patrick Ogenstad)
Networklore Toolkit (Nelkit) is a collection of free tools aimed to help network engineers.
* https://networklore.com/nelkit
* https://networklore.com/nk-compare-configs

## Front ends 
(really more like 'getting severely sidetracked')    
*  https://www.airpair.com/python/posts/django-flask-pyramid

###     DJANGO
Django is a high-level Python Web framework that encourages rapid development and clean, pragmatic design. 
* https://www.djangoproject.com/
* https://docs.djangoproject.com/en/1.9/intro/tutorial01/
* https://www.turnkeylinux.org/django

###     Pyramid
similar purpose to Django
* https://trypyramid.com/
* http://www.pylonsproject.org/

###     Flask
similar purpose to Django but simpler
* http://flask.pocoo.org/
* https://pypi.python.org/pypi/Flask/0.11

###     Waitress
Waitress is meant to be a production-quality pure-Python WSGI server with very acceptable performance. It has no dependencies except ones which live in the Python standard library.
* http://docs.pylonsproject.org/projects/waitress/en/latest

###     Postman
Roll your own API... 
https://www.getpostman.com


## Utilities

DNS (the virtual world)
* https://www.turnkeylinux.org/forum/general/20110413/simplest-dns-server
* http://www.virtualizationhowto.com/2015/04/lightweight-dns-server-vmware-lab/

