# ormucotest-ansible-django

## Steps to deploy Django Application with Apache using Ansible 

#### 1- Install Ansible 
     $ sudo apt-get update
     $ sudo apt-get install ansible 
           
#### 2- Generate a RSA Key Pair for authentication without password on the client machine
     $ ssh-keygen -t rsa
     $ ssh-keygen -t rsa -b 2048 -v     
      
     Once you have entered the Gen Key command, you will get a few more questions, you can press enter here.
     
#### 3- Copy the public on the virtual server that we want to use
     $ ssh-copy-id root@your-ip-address    
                 
#### 4- Clone Ansible Repository
     $ git clone https://github.com/lauricdd/ormucotest-ansible-django.git
      
#### 5- Customize hosts files
     $ cd ormucotest-ansible-django
     $ nano hosts

     output-examle:
     [servers]
     *your-ip-address
  
#### 6- Run deploy.yml ansible playbook
     $ cd ormucotest-ansible-django
     $ ansible-playbook -i ./hosts deploy.yml


#### 7- Check on browser 
     https://your-ip-address
