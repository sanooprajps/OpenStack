Openstack Rocky Manual Installation (Ubuntu 18.04)<br>
-------------------------------------------------
1. Openstack packages for Ubuntu<br>
https://docs.openstack.org/install-guide/environment-packages-ubuntu.html

2. SQL Database<br>
Most OpenStack services use an SQL database to store information. The database typically runs on the controller node. MariaDB or MySQL or PostgreSQL can be used.
MariaDB will be used here.

https://docs.openstack.org/install-guide/environment-sql-database-ubuntu.html

3. Message Queue<br>
OpenStack uses a message queue to coordinate operations and status information among services. 
The message queue service typically runs on the controller node. OpenStack supports several message queue services including RabbitMQ, Qpid, and ZeroMQ.
RabbitMQ will be used here.

https://docs.openstack.org/install-guide/environment-messaging-ubuntu.html

4. Memcached<br>
The Identity service authentication mechanism for services uses Memcached to cache tokens. The memcached service typically runs on the controller node.

https://docs.openstack.org/install-guide/environment-memcached-ubuntu.html

5. Etcd<br>
OpenStack services may use Etcd, a distributed reliable key-value store for distributed key locking, storing configuration, keeping track of service 
live-ness and other scenarios.

https://docs.openstack.org/install-guide/environment-etcd-ubuntu.html

Openstack Core Services<br>
------------------------

1. Identity Service - Keystone <br>
https://docs.openstack.org/keystone/rocky/install/keystone-install-ubuntu.html

Check /var/log/keystone and make sure there are not database connection error. If yes, loginto mysql -> keystone database and see if you are able to see many tabels.
If not check /etc/hosts for controller IP, make mysql listen on all hosts, and rerun populate command.

2. Image Service - Glance <br>
https://docs.openstack.org/glance/rocky/install/install-ubuntu.html

3. Compute Service - Nova <br>
https://docs.openstack.org/nova/rocky/install/

Both controller and compute needs to be installed.
This configuration uses the Quick EMUlator (QEMU) hypervisor with the kernel-based VM (KVM) extension on compute nodes that support hardware acceleration for virtual machines.

4. Networking service <br>
https://docs.openstack.org/neutron/rocky/install/install-ubuntu.html

Both controller and compute needs to be installed.
Select Networking Option 2: Self-service networks, this should have both provider and self-service networks.

5. Dashboard - Horizon <br>
https://docs.openstack.org/horizon/rocky/install/install-ubuntu.html
The only core service required by the dashboard is the Identity service.

6. Block Storage - Cinder <br>
