# redmine-rockylinux8-ansible

Ansible playbook to build redmine on Rocky Linux 8.

---
## Environment

* Rocky Linux 8.6: AlmaLinux 8.6 compatible
* postgresql
* nginx
* ruby: 2.7.x
  - rbenv
  - unicorn
  - redmine: 4.2-stable

* aws: t3.medium
* ibmcloud: bx2-2x8


---
## Require Ansible Collections
* ansible.posix
* community.general
* community.postgresql

---
## Usage

### 1.　clone repository

```
$ git clone https://github.com/yasu0519/redmine-rockylinux8-ansible.git
```

### 2.　inventory setup

```
$ vi redmine-rockylinux8-ansible/inventories/hosts
```

```
[redmine]
xxx.xxx.xxx.xxx ansible_user=root ansible_ssh_private_key_file="/path/to/private_key"
```

* xxx.xxx.xxx.xxx: Specify the IP address or host name of the host you want to install.
* /path/to/private_key: Specify the file path of the private key of the host to install.

### 3.　run playbook

```
$ cd redmine-rockylinux8-ansible
$ ansible-playbook redmine.yml
```
