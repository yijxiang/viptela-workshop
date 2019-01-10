# Exercise 1.0 -  Using Ansible with Viptela SDx Workshop

## Requirements

* pip: `pip install -r requirements.txt`
* sshpass


## Step1

Cloning the workshop repo repo:

git clone `https://github.com/ciscops/viptela-workshop.git`


## Step 2

Navigate to the `viptela-workshop` directory.

```
$ cd viptela-workshop/
```

>Note: All subsequent exercises will be in this directory unless otherwise noted.

## Step 3

Deploy Topology:

Create a .virlrc:
```
VIRL_USERNAME=guest
VIRL_PASSWORD=guest
VIRL_HOST=your.virl.server
```

Run the `build` playbook to the build the topology:
```
ansible-playbook build.yml
```

This playbook will:
* Launch the topology file
* Wait until they show as reachable in VIRL

>Note: Other topologies can be built using the `topo_file` extra var:
```
ansible-playbook build.yml -e topo_file=other_topology.virl
```
