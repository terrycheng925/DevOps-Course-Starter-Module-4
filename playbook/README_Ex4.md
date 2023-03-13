# DevOps
This is Model 4 ex.


## Getting started

setup  
 controller host : 
   #3.8.224.35 
   217.174.244.34

 target host :
   #18.132.86.249
   109.228.38.127



in controller host :
/home/ec2-user/
-rw-rw-r-- 1 ec2-user ec2-user   31 Oct 10 17:00 my_inventory.yml
drwxrwxr-x 2 ec2-user ec2-user   20 Oct 14 14:17 template
-rw-rw-r-- 1 ec2-user ec2-user 3281 Oct 14 15:11 first_playbook_file.yml

- my_inventory.yml        - define the target host
- first_playbook_file.yml - define all the tasks 
- template                - defin the env template file 


1. setup the ssh key for both hosts

ssh to controller host to execuate the ansible playbook.
2. ssh ec2-user@3.8.224.35
  
[ec2-user@ip-10-0-0-88 ~]$ pwd
/home/ec2-user
[ec2-user@ip-10-0-0-88 ~]$ ls -lrt
total 8
-rw-rw-r-- 1 ec2-user ec2-user   31 Oct 10 17:00 my_inventory.yml
drwxrwxr-x 2 ec2-user ec2-user   20 Oct 14 14:17 template
-rw-rw-r-- 1 ec2-user ec2-user 3281 Oct 14 15:11 first_playbook_file.yml

to execuate the command :
> ansible-playbook first_playbook_file.yml -i my_inventory.yml


3. check the result, ssh to the target host
  > ssh ec2-user@18.132.86.249

#to check the result for using template:
> cd /home/ec2-user
> ls -la .env 

#to check the result for poetry installation:
> cd /etc/poetry
> ls -l /etc/poetry
> poetry --version

# to check the result for the todo apps:
> cd /opt/todoapp
> ls -l 









