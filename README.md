Docker
======

Ansible role that does an opinionated installation of the Docker daemon on Debian
systems.

Requirements
------------

Docker daemon will be configured to log using journald.

Docker networking is disabled by default for mainstream firewall
(UFW/Firewalld) management software compatibility.

PIP is required to install the Docker python package so it can be used by
Ansible container tasks.

Role Variables
--------------

Available variables are listed below, along with default values (see
`defaults/main.yml`):

	docker_users:
	  - "{{ ansible_user }}"

Users that are allowed to access the Docker daemon.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: git+https://github.com/basvdlei/ansible-role-docker.git,
             name: basvdlei.docker }

License
-------

BSD 3-Clause
