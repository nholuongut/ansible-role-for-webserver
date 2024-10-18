# Ansible Role: Webserver (Nginx OR Apache)

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

This role installs and configure a webserver. For the moment, this role only manages *Nginx* OR *Apache* (you can choose which one to install using a variable).

The following actions are performed:
- Install the latest version of Nginx or Apache
- Install the latest version of PHP-FPM
- Install the latest version of UFW
- Remove the default Website of the Web server
- Copy some hardened website templates to /root/
- Open the HTTP and HTTPS ports in the firewall
- Prepare the skeleton of new users to handle Websites

Requirements
------------

No specific requirements for this role.


Role Variables
--------------

By default, this role will install and configure Nginx. However, a variable can be set to choose Apache if you want to.

Here is the variable as defined by default in this role:

```
webserver: nginx
```

If you prefer to install Apache instead of Nginx, set the value of this variable to *apache*.


Dependencies
------------

No dependencies from other roles required.


Example Playbook
----------------

Here is a simple example playbook to use this role:

```
hosts: web_srv
user: root
roles:
  - { role: webserver, tags: [ 'webserver' ] }
```

TODO
----

Some hardening & comments remains to be done about Web servers. Here is the list:

- Fake the server information (global config)
- Configure certain modules (mod_security or other WAF)
- Update this README to explain various actions (ex.: calculate HPKP)


# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
