Ansible Assignemt - Arctiq

 - Provision VM
 - Deplpoy WebApp
 - Teardwon VM

Prerequsites:
- All required files and playbooks to provision, deploy and terminate/teardown are ansible-assignment directory
- It's committed to git
- vars.yml and ansible-assignment.pem files are needed
- They should reside right outside ansible-assignment
- Also AWS isn't accepting ansible-assignment.pem file with 644 perms
- Please change it to 600 on your machine

Provision VM:
- Please use ec2-create.yml to provision EC2 VM on AWS
- Also please run ec2-info.yml to get the public dns of EC2 added to host for ease of use

Deploy Webapp:
- Use ec2-webapp.yml playbook to deploy Nginx and a sample site on EC2 instance
- Use the below command:
	ansible-playbook --private-key=../ansible-assignment.pem ec2-webapp.yml

Teardown VM:
- This is a simple straight forward playbook that just deletes exisiting EC2 VM
- Use ec2-tear.yml playbook to do that

echo "options rtl8723be ant_sel=2"  >  /etc/modprobe.d/rtl8723be.conf
