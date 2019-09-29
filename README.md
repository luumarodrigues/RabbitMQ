# RabbitMQ
Ansible playbook to install RabbitMQ

## Roles: 
     - Deploy-rabbimq
     - Deploy-rabbimq-config

## Roles Variables

Set in defaults/main.yml

### Role: Deploy-rabbimq
 
    rabbitmq_erlang_cookie: "EAANDECMWRUOYGDIEDRL"

    rabbitmq_cluster_master: "cluster-rabbitmq"
    rabbitmq_plugins:
      - rabbitmq_management
      - rabbitmq_management_agent
    
    rabbitmq_use_longname: 'true'
    log_base: "/rabbitmq/log"
    mnesia_base: "/rabbitmq/mnesia"
    config_file: "/etc/rabbitmq"    

### Role: Deploy-rabbimq-config

    user: 'admin'
    password: 'admin'

## Inventory
Simple text file with the IP of the machine to be manipulated
It can have any name, it's passed as a parameter -i
```
$ ansible-playbook -i inventory
```
Contents of the hosts file
```
[targets]
localhost
```

## Initial Setup

Configure the IP of the machine from which you want make the configuration host requirements in
```
$ vim inventory
```

## Usage and Example Playbook
```
$ git clone 
```

## Run the playbook

```
$ ansible-playbook -i inventory main.yml
```