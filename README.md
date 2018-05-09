About:
  This is a Ansible Galaxy role that installs ActiveMQ and run it inside a Supervisord service.

  It will fail on OS's that are not supported. Currently Supported:
    - Centos 6
  Fail condition is tasks/main.yml

Configure:
  There are some variables used in this role inside the 'defaults/main.yml' conf file. 

  activemq:
    version: the version of ActiveMQ to install.  Defaults to version '5.14.3'.
    path: the path to extract the tar ball to. Defaults to '/opt'.

  java:
    version: the version of java to install.  Defaults to version '1.8.0'.

  You can run certain pieces of the role via tags. 
  
  Naming conventions: 
  - *-install, installs the binary
  - *-env, exports os environment variables
  - *-check, conditional gate to proceed with tasks
  - *-conf, copys configuration files over to client server
  Available tags:
  - os-check
  - basics
    - basics-install 
  - java
    - java-env 
    - java-install 
  - activemq
    - activemq-check
    - activemq-env
    - activemq-install
  - supervisord
    - supervisord-conf 
    - supervisord-install

Future To Do's:
  - Transition from using to shell scripts where possible to ansible modules.
    + Unarchive and Ip tables modules were producing unexpected results when attempted. Debugging required. 
  - Support activemq clustering
