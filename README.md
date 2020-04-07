# Ansible-Kubernetes
----------------------------------------------------------------------------------------------------------------------------------------
# put 3 EC2 instances 
    1.   Ansible Controller
    2.   k8s Master t2.medium 4GB RAM, 2CORE
    3.   the node
----------------------------------------------------------------------------------------------------------------------------------------

# create a directory in ansible controller
          mkdir kubernetes
          put all the playbooks for master as well as node over here.
          
----------------------------------------------------------------------------------------------------------------------------------------

# do ssh-keygen on both k8s master and the node
      test all the host using ssh ubuntu@<ip_addr_machine>

----------------------------------------------------------------------------------------------------------------------------------------
# edit the host.ini file

    put your master and node ip address: hostname ansible_ssh_host=<ip_addr>

----------------------------------------------------------------------------------------------------------------------------------------
# ping your hosts from ansible controller
    ansible -m ping all

----------------------------------------------------------------------------------------------------------------------------------------
# run the site.yaml file from ansible controller
    ansible-playbook site.yaml

----------------------------------------------------------------------------------------------------------------------------------------

#  for server hardening change the outbound rules of the instances to HTTP/HTTPS and choose the ip as anywhere.
