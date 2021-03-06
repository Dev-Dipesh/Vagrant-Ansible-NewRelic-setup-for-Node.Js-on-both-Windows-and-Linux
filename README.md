![Alt](https://raw.githubusercontent.com/Dev-Dipesh/Vagrant-Ansible-NewRelic-setup-for-Node.Js-on-both-Windows-and-Linux/master/img/ansibleVagrantNodeRelic.png)
SETUP YOUR DEV ENVIRONMENT
==========================

This is a setup repository to guide you threw the process of setting up **Ansible** and **Vagrant** with **New Relic** for a **node.js** based web application. It will also showcase you how to provision your **Vagrant Boxes** with **Ansible** and on top of it in OS, even on **Windows** where Ansible is not supported directly.

Another big deal it covers is **automated setup of New Relic via Ansible for machine OS monitoring**.

If anyone have any queries than feel free to raise it.

Vagrant Setup
-------------

 - Precise32 Box
 - Port Forwarding
 - Private Network
 - Public Network
 - Sync Folders
 - Allocating Custom Memory and CPUs
 - Configuring to use Ansible's Playbooks written in Python Jinja2 Template

Ansible Setup
-------------

 - Basic Linux Packages
 - Node.JS
 - Coffee Script
 - Node Modules
 - Grunt
 - Grunt-cli
 - MySQL
    - Installing MySQL
    - Setting Up Config File
    - Altering Databases
    - Running MySQL service
 - New Relic for System Monitoring
 - MongoDB
 - CSS
 - SASS
 - LESS
 - ElasticSearch
 - GodBox

 **NOTE: Remember to add your New Relic key in Ansible `playbook.yml`**

ANSIBLE PROVISIONING
--------------------
![Alt](https://raw.githubusercontent.com/Dev-Dipesh/Vagrant-Ansible-NewRelic-setup-for-Node.Js-on-both-Windows-and-Linux/master/img/Ansible%20Server%20Box%20Setup.png)

SYSTEM MONITORING IN NEW RELIC
------------------------------
![Alt](https://raw.githubusercontent.com/Dev-Dipesh/Vagrant-Ansible-NewRelic-setup-for-Node.Js-on-both-Windows-and-Linux/master/img/2014-09-10%2013_58_02-local%20-%20New%20Relic.png)

NODE APPLICATION RUNNING
------------------------
![Alt](https://raw.githubusercontent.com/Dev-Dipesh/Vagrant-Ansible-NewRelic-setup-for-Node.Js-on-both-Windows-and-Linux/master/img/2014-09-03%2016_29_18-PM2%20Running%20clusters.png)