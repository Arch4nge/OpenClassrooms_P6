# OpenClassrooms_P6
A docker powered lab with ansible automation for a load-balanced basic web app.


# How tu run the lab ?
Simply run `docker-compose up -d`
Then execute `ansible-playbook playbook.yml -i inventory` in the main directory.


# Customisation of the lab
You can change docker options in the docker-compose.yml file
(example change how many web server are running)

If you add more or less docker containers you have to specify them in the inventory file of ansible in [web] part.

You can also change actions executed on theses containers in the playbook.yml file.

Web app configuration is in files dir.
Load-balancing configuration is in templates dir.
