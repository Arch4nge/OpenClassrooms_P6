# OpenClassrooms_P6
A docker powered lab with ansible automation for a load-balanced basic web app.


# How tu run the lab ?
Simply run clone the repo and specify :
- The repo of your php web project repository in playbook.yml
- Your infrasture machines addresses in the inventory file


# Customisation of the lab
You can changes everything you want in configs files.

To change web-deployer role go in "role/web-deployer" folder

To change load-balancing role go in "role/load-balancing" folder

# Attention

Be careful, the load-balancing role is using a "web" group in order to create the nginx template

# Example
```
- hosts: load_balancing
  become: true
  roles:
    - load-balancer
- hosts: web     # the group that load-balncer iterate on
  become: true
  roles:
    - role: web-deployer
      repo: 'INSERT_YOUR_REPO_URL_HERE'
```
