# Roboshop-Ansible
Config Mgmt Automation 

Basic ,
 inventry have created in smae path 

 [ec2-user@user ~/Roboshop-Ansible ]$ ansible-playbook -i inv  basic.yaml -e "ansibel_user=ec2-user ansible_password=DevOps321"


[ ec2-user@user ~/Roboshop-Ansible ]$ ansible -i inv all  -e "ansible_user=ec2-user ansible_password=DevOps321" -m ansible.builtin.shell -a "ls /home/ec2-user"

ansible all -i inv -l dev -e "ansible_user=ec2-user ansible_password=DevOps321" -m ansible.builtin.package -a "name=nginx state=absent" --become

ansible all  -i inv -e "ansible_user=ec2-user ansible_password=DevOps321" -m ansible.builtin.shell -a "ps -ef | grep -i nginx"

run only on prod inventory with tags define to task perform end 

 ansible-playbook  -i inv -l prod package.yaml -e "ansibel_user=ec2-user ansible_password=DevOps321" --become --tags=check

[ ec2-user@admin ~/Roboshop-Ansible/roboshop ]$ git pull

[ ec2-user@admin ~/Roboshop-Ansible/roboshop ]$ ls  Diectory structure 
inventory  roboshop.yaml  roles

once roles created / Final commands 

[ ec2-user@admin ~/Roboshop-Ansible/roboshop ]$ ansible-playbook -i inventory -e ansible_user=ec2-user -e ansible_password=DevOps321 roboshop.yaml -e env=dev -e component=frontend

