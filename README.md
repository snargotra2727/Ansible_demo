# Ansible_demo

This Ansible playbook is designed to automate the process of installing and configuring NGINX on a production server, and then deploying a static website. Here's an explanation of what it does:

Ansible Playbook Breakdown:
Name of the Playbook: Install NGINX and Serve Static Website.

Hosts: This playbook will run on servers or hosts under the inventory group prod, which likely refers to production servers.

Privilege Escalation: become: yes ensures that tasks requiring elevated privileges (like installing software or managing services) are executed with sudo permissions.

Tasks:

Install NGINX:
Uses the apt module to install the latest version of the NGINX web server.
Start and Enable NGINX:
Uses the service module to start the NGINX service and ensures it is enabled to automatically start on boot.
Deploy Web Page:
Uses the copy module to copy a local index.html file (static website) from the Ansible control node to the server’s /var/www/html directory, which is the default document root for NGINX.
