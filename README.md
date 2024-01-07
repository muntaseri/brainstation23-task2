# brainstation23-task2
brainstation23-task2


vagrant install in ubuntu

wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install vagrant



Step 1: Creating a Vagrantfile
Use the text editor of your choice and create a file with named Vagrantfile, inserting the code below. The value of N denotes the number of nodes present in the cluster, it can be modified accordingly. In the below example, we are setting the value of N as 2.

check the Vagrantfile included onthe repository.





Step 2: Create an Ansible playbook for Kubernetes master.
Create a directory named kubernetes-setup in the same directory as the Vagrantfile. Create two files named master-playbook.yml and node-playbook.yml in the directory kubernetes-setup.


Step 3: Power up vagrant 

$ vagrant up



Step 4: Verify on master



$ vagrant ssh k8s-master
$ kubectl get nodes
NAME         STATUS   ROLES                  AGE     VERSION
k8s-master   Ready    control-plane,master   5m6s    v1.23.0
node-1       Ready    <none>                 2m59s   v1.23.0
node-2       Ready    <none>                 68s     v1.23.0



