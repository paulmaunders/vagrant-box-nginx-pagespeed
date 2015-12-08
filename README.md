# vagrant-nginx-pagespeed
A vagrant file with associated ansible provisioning to test my nginx pagespeed role.

# Instructions
To use this vagrant environment, firstly clone the project, then run...
```
ansible-galaxy install -r requirements.yml
vagrant up
```
**NB**: I normally run this on a lab server and so I have enabled external port forwarding  by default in the vagrant file. This means that any host on your network will be able to access nginx on the vagrant box through port 8080. You can disable this by setting the gateway_ports option to false in the Vagrant file.
```
 config.vm.network "forwarded_port", guest: 80, host: 8080, gateway_ports: true, host_ip: "*"
```
