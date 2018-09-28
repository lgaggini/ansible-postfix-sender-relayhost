# ansible-postfix-sender-relayhost

ansible-postfix-sender-relayhost is an Ansible role to install and configure postfix as a sender dependent relayhost on a debian based OS.

It performs: 

* installation of postfix package(s)
* configuration of submission service
* configuration of sasl authentication for smtpd and smtp
* configuration of multiple sender dependent relayhosts

## Install
### Clone
```bash
git clone https://github.com/lgaggini/ansible-postfix-sender-relayhost.git
```
## Configuration

The configuration is done by vars listed and explained in [defaults/main.yml](https://github.com/lgaggini/ansible-postfix-sender-relayhost/blob/master/defaults/main.yml) file.

## Usage

```
- name: bootstrap an ubuntu cloud image for dovecot
  hosts: mailserver
  vars_files:
    - group_vars/postfix.yml

  roles:
    - { role: postfix-sender-relayhost, tags: ['postfix-sender-relayhost'] }
```
