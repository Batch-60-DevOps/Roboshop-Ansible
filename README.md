# Roboshop-Ansible
Config Mgmt Automation 

Basic ,
 inventry have created in smae path 

 [ec2-user@user ~/Roboshop-Ansible ]$ ansible-playbook -i inv  basic.yaml -e "ansibel_user=ec2-user ansible_password=DevOps321"


[ ec2-user@user ~/Roboshop-Ansible ]$ ansible -i inv all  -e "ansible_user=ec2-user ansible_password=DevOps321" -m ansible.builtin.shell -a "ls /home/ec2-user"


ansible all  -i inv -e "ansible_user=ec2-user ansible_password=DevOps321" -m ansible.builtin.shell -a "ps -ef | grep -i nginx"

run only on prod inventory with tags define to task perform end 

<<<<<<< HEAD
 ansible-playbook  -i inv -l prod package.yaml -e "ansible_user=ec2-user ansible_password=DevOps321" --become --tags=check
=======
 ansible-playbook  -i inv -l prod package.yaml -e "ansibel_user=ec2-user ansible_password=DevOps321" --become --tags=check

>>>>>>> 6c4f943 (robo1)
