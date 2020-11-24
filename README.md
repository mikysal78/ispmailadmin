Ansible Role ISPmail Admin
=========

Role to install and upgrade ISP Mail Admin

Package of:
[ISPmail Admin by Ole Jungclaussen](https://www.ima.jungclaussen.com)

[Demo Version](Demo https://www.ima.jungclaussen.com/demo/)

Requirements
------------

Mail server and Web Server (LEMP or LAMP).

I using this role:
[Ansible Role Postfix-Dovecot fork from @StackFocus](https://github.com/mikysal78/ansible-role-postfix-dovecot)
and
[Ansible Mysql of @HanXHX](https://github.com/HanXHX/ansible-mysql)


Role Variables
--------------

Any variables that are in defaults/main.yml


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```yml
- hosts: mail
  become: "{{ become | default('yes') }}"
  roles:
    - { role: ispmailadmin, tags: ispmailadmin }

  vars:
    ispmailadmin_htdocs: /var/www/ispmailadmin
    ispmailadmin_db_user: db_user
    ispmailadmin_db_pass: db_pass
    ispmailadmin_db_name: mailserver
    ispmailadmin_user: admin_user
    ispmailadmin_pass: admin_pass
```

License
-------

GPL

Author Information
------------------

- [MikySal78](https://github.com/mikysal78)
