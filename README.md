# Project-deployment-Github-Jenkins-Ansible-Webnodes
Project to install appache in webnode servers through jenkins using ansible playbook

Github to Jenkins to Ansible Master to deploy in webnodes 

Step –1 launch 2 web nodes EC2 instances in AWS 

Step –2 then do a password less authuntication setup with both web nodes into ansible master            by creating a new user 

Step –3 go to ansible master, update the hosts file with the correct private ip addresses of the               webnodes 

Step –4 then copy the ssh key from ansible master to webnodes through ssh-copy-id username@private_ip_address 

Step-5 then check the connection between the web-nodes and master by ansible all –m ping                 the output should be ping : pong  

Step-6 Copy the public key from jenkins machine to ansible master. And set continues flow from jenkins master to ansible master to the webnodes. 

Step-7 then create a new repository in git hub and upload a playbook.yaml file having the script. 

Step-8 Go to jenkins open a freestyle pipeline and create a connection between github remot repository and jenkins pipeline. 

Step-9 instal Ansible – master sever info in jenkins then click on manage jenkins goto systems then install the server using correct host name and other info. 

Step-10 add the jenkins server to the pipeline and through executable command run the ansible-playbook -I /etc/ansible/hosts playbook.yaml 

Then build the pipeline.  
