## Main goal
Set up different environments using Vagrant, Ansible, Docker and Jenkins.

**Resolution:**
I created a Vagrantfile in which use the following addresses:
- IP_DEV    = "10.46.20.21"
- IP_QA     = "10.46.20.22"
- IP_UAT    = "10.46.20.23"
- IP_PROD   = "10.46.20.24"
- IP_jenkins= "10.46.20.25"

Vagrant image: "debian/stretch64"

In each environment (except for jenkins server) will set up an Wordpress Application which will be inside a Docker container, the ports that  will use are:
- Nginx: 80
- DB: 3306
- Wordpress: 9000
- Jenkins: 8080

**Prerequisites**

- You must have installed:
  - Virtualbox
  - Vagrant
  - Ansible
  - Docker
  - Git

- - -
Clone the repository:

`git clone https://github.globant.com/jorge-contti/Week2.git`

Go to Vagrant folder where the Vagrantfile is located and execute the following: 

`sudo vagrant up`

<br/>

The environments will be setting up in this order: 
    dev > qa > uat > prod > jenkins

<br/>

To enter in each application you have to use the IP of each VM, example: 
http://10.46.20.22

Do the same to enter in Jenkins but adding the port 8080: 
http://10.46.20.25:8080

<br/>

**Useful Links:**

 - Ansible and Vagrant
 
(https://blog.deiser.com/es/primeros-pasos-con-ansible)

(https://docs.ansible.com/ansible/latest/scenario_guides/guide_vagrant.html)

(https://www.digitalocean.com/community/tutorials/configuration-management-101-writing-ansible-playbooks)

(https://www.simonholywell.com/post/2016/02/intelligent-vagrant-and-ansible-files/)

(https://www.taniarascia.com/what-are-vagrant-and-virtualbox-and-how-do-i-use-them/)

 - Docker
 
https://docs.docker.com/get-started/

https://www.youtube.com/watch?v=UZpyvK6UGFo&list=PLqRCtm0kbeHAep1hc7yW-EZQoAJqSTgD-&index=2&t=3s

 - Jenkins
 
(https://github.com/jenkinsci/docker/blob/master/README.md)

(https://wiki.jenkins.io/display/JENKINS/Publish+Over+SSH+Plugin)



