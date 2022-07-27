Vagrant Experiment
---

### Instructions
```sh
git clone https://github.com/ivoputzer/vagrant-experiment-2.git
cd vagrant-experiment-2

vagrant up --provision
ansible all -i inventory -m ping -v
```
