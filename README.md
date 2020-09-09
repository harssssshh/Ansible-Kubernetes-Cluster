# Ansible-Kubernetes-Cluster
### Create SSH Key Using ssh-keygen

`ssh-keygen`

![Alt text](/Screenshots/ssh-keygen.png?raw=true "SSH-Keygen")

### Copy Public Key

`cat ~/.ssh/id_rsa.pub`

![Alt text](/Screenshots/ssh-keygen-2.png?raw=true "SSH-Keygen")

## Add SSH Key To DigitalOcean

![Alt text](/Screenshots/do-ssh-1.png?raw=true "Digitalocean SSH")

### Copy SSH Key To DigitalOcean

![Alt text](/Screenshots/do-ssh-2.png?raw=true "Digitalocean SSH")

## Creating Droplets

### Choosing Droplet Size

![Alt text](/Screenshots/do-vps-1.png?raw=true "Digitalocean SSH")

### Choosing SSH-Key & Naming Droplets

![Alt text](/Screenshots/do-vps-2.png?raw=true "Digitalocean SSH")

### Droplets

![Alt text](/Screenshots/do-vps-3.png?raw=true "Digitalocean SSH")

### Install Ansible
`sudo apt-get install ansible`


### Configuring hosts file

![Alt text](/Screenshots/hosts.png?raw=true "Digitalocean SSH")

### Applying Initial Configuration

`anisble-playbook -i hosts inital.yaml`

![Alt text](/Screenshots/ansible-1.png?raw=true "Digitalocean SSH")

### Applying Kubernetes Dependencies

`anisble-playbook -i hosts kubernetes-dependencies.yaml`

![Alt text](/Screenshots/ansible-2.png?raw=true "Digitalocean SSH")

### Applying Master Node Configuration

`anisble-playbook -i hosts master.yaml`

![Alt text](/Screenshots/ansible-3.png?raw=true "Digitalocean SSH")

### Applying Worker Node Configuration

`anisble-playbook -i hosts workers.yaml`

![Alt text](/Screenshots/ansible-4.png?raw=true "Digitalocean SSH")

### Checking Nodes

`ssh -i ~/.ssh/id_rsa kubeadmin@<master-node-ip>`

`kubectl get nodes`

![Alt text](/Screenshots/final.png?raw=true "Digitalocean SSH")
