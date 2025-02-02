### Prereqs

- Virtualbox per https://www.virtualbox.org/ and add your username to the vboxusers group in /etc/group followed by a relogin
- Get Hashicorp vagrant from https://developer.hashicorp.com/vagrant/install?product_intent=vagrant
- Ansible: apt-get/dnf install ansible


### Installation / setup

- clone the git repo
- run vagrant up and follow the progress


### Checks and changes

- To run just the sanity checks: vagrant ssh -c "cd /data && ansible-playbook --extra-vars @variables.yml -i inventory check-nginx.yml" 
- Updates can me made by changing data/variables and running destroy / up with vagrant or check the playbooks from the Vagrantfile and run with via vagrant ssh



 *to be used on a "normal" linux host, otherwise your mileage may vary*
