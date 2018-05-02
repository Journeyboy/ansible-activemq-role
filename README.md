About:
  This is a Ansible Galaxy role that installs ActiveMQ and run it inside a Supervisord service.

Configure:
  There are some variables used in this role inside the 'defaults/main.yml' conf file. 

  activemq:
    version: the version of ActiveMQ to install.  Defaults to version '5.14.3'.
    path: the path to extract the tar ball to. Defaults to '/opt'.

  java:
    version: the version of java to install.  Defaults to version '1.8.0'.


