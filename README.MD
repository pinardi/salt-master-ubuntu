install salt master ubuntu**Table of Contents**

* [Installation](#installation)
* [activate service salt](#activated)
* [edit configuration](#edit)
* [restart service salt master dan minion](#restart)
* [show list key has been connect from minion to master](#show)
* [authorize the listed minions](#authorize)
* [permit all keys with "A" option](#permit)

# Installation
## install & download salt di CentOS
```bash
```bash
apt-get install salt-api
apt-get install salt-cloud
apt-get install salt-master
apt-get install salt-ssh
apt-get install salt-syndic
```

```
# activated
## start & activated service salt-master
```bash
systemctl start salt-master.service
systemctl enable salt-master.service
```

# edit
## salt master
```bash
nano /etc/salt/minion
master: "ip of salt master"
```
# restart
## restart service salt master
```bash
systemctl salt-master start
systemctl enable salt-master
```
# show
## show list key has been connect from minion to master
```bash
salt-key -L
```
# authorize
## authorize the listed minions
```bash
salt-key -A
```

# permit
## permit all keys with "A" option

```bash
salt-key -A 
The following keys are going to be accepted:
Unaccepted Keys:
node01.srv.world
Proceed? [n/Y] y Key for minion node01.srv.world accepted.

salt-key -L 
Accepted Keys:
minion
Denied Keys:
Unaccepted Keys:
Rejected Keys:
```
