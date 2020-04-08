Role Name
=========

Ce role ansible permet d'installer [Auditd](https://github.com/tassyk/security/blob/master/hardening_auditing_system.md) sur une machine Linux Centos 7.

Auditd est un outil permettant de monitorer l'intégrité des systèmes de fichiers.
 
Il pousse un certain nombre de règles pour monitorer certains fichiers du système.

Requirements
------------


Role Variables
--------------

Les variables par défaut sont renseignés dans default/main.yml :
```
- default_rules: règles par défaut
- custom_rules: règles personnalisées
```
Dependencies
------------

Le rôle peut être intégré facilement dans d'autres projets. Pour ce faire :
- créer un fichier **requirements.yml** avec le contenu ci-dessous :
```
---
- name : auditd
  src : https://github.com/tassyk/ansible-auditd.git
  scm: git
  version : origin/master
```
- Installer le rôle avec ansible Galaxy :
```
ansible-galaxy install -r requirements.yml -p /chemin/repertoire/roles
```
Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      remote_user: user
      become: True
      roles:
      - ansible-auditd

Exemple d'exécution du playbook :
```
ansible-playbook auditd.yml -i hosts -u user
```

License
-------

TassyK

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
