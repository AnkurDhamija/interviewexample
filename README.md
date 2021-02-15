How to Create Jenkins Pipeline
1. Pipeline has been created using Blueocean
2. Upload the file to git repo and connect to Blueocean
3. Provide inventory file for ansible-playbook
4. Trigger the Pipeline

Sample inventory File ->
[all]
server ansible_host=ip_address ansible_user=ubuntu ansible_ssh_private_key_file=path_to_private_key
