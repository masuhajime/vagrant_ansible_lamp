centos65 lamp
====

```
$ ansible-galaxy install
    - geerlingguy.repo-epel
    - geerlingguy.mysql
    - geerlingguy.apache
    - geerlingguy.php
    - geerlingguy.redis
```

```
Host vm
    HostName        192.168.33.10
    User            masuhajime
    IdentityFile ~/.vagrant.d/insecure_private_key
    Port 22
```

```
$ vagrant up --provision
$ ssh vm
```
