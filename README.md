# rocket-chat-ansibled

Playbooks and files to deploy Rocket chat server, in docker containers, on a random server.

## How to use

First, download the roles required:

	sudo ansible-galaxy install -r requirements.yml

Then, fill the inventory file:

	cp hosts.example hosts
	sed -i 's/myserver.example.com/realserver.realdomain.com/' hosts

Finally, run the playbook:

	ansible-playbook -i hosts main.yml
