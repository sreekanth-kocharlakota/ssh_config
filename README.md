# ssh_config
A simple and common use case is to access a VM DB System (or any host in a private subnet). Since it's not recommended to put a database in a public subnet you need to access it via a bastion host. Either you have a dedicated bastion host or you can use any compute instance with a public IP that you have access to and that sits in the same VCN. In my use case, I want to use tools like SQL Developer, DBeaver, HeidiSQL (Windows) to connect directly to the database via the bastion host or GUI apps like FileZilla to copy files, RDP clients for Windows hosts, VNC clients etc.. Then it's both convenient and secure to create an ssh tunnel and forward these remote ports to your local machine.

In this test setup, the VCN has two subnets, one public and one private. All security lists and route tables are default.

![alt text](https://github.com/sreekanth-kocharlakota/ssh_config/blob/main/bastion_host_usage.jpeg?raw=true| width=100)

