Openstack Rocky Manual Installation (Ubuntu 18.04)
-------------------------------------------------
1. Openstack packages for Ubuntu
https://docs.openstack.org/install-guide/environment-packages-ubuntu.html

2.SQL Database
Most OpenStack services use an SQL database to store information. The database typically runs on the controller node. MariaDB or MySQL or PostgreSQL can be used.
MariaDB will be used here.

https://docs.openstack.org/install-guide/environment-sql-database-ubuntu.html

3. Message Queue
OpenStack uses a message queue to coordinate operations and status information among services. 
The message queue service typically runs on the controller node. OpenStack supports several message queue services including RabbitMQ, Qpid, and ZeroMQ.
RabbitMQ will be used here.

https://docs.openstack.org/install-guide/environment-messaging-ubuntu.html

4. Memcached
The Identity service authentication mechanism for services uses Memcached to cache tokens. The memcached service typically runs on the controller node.

https://docs.openstack.org/install-guide/environment-memcached-ubuntu.html

5. Etcd
OpenStack services may use Etcd, a distributed reliable key-value store for distributed key locking, storing configuration, keeping track of service 
live-ness and other scenarios.

https://docs.openstack.org/install-guide/environment-etcd-ubuntu.html

Openstack Core Services
------------------------

1. Identity Service - Keystone 
https://docs.openstack.org/keystone/rocky/install/keystone-install-ubuntu.html

2. 
