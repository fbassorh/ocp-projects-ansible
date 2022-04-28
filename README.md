# ocp-projects-ansible
Pass vault: redhat01

Viene con el collection redhat.openshift por default, pero están comentadas las líneas para usar el comunitario community.okd
Para el uso de el collection redhat.openshift se debe configurar ansible.cfg en la raíz del proyecto

PASOS:

1. Install requests-oauthlib
	$ pip3 install requests-oauthlib
2. Install kubernetes
	$ pip3 install kubernetes
3. Creaet ansible.cfg
	[galaxy]
	server_list = automation_hub

	[galaxy_server.automation_hub]
	url = https://cloud.redhat.com/api/automation-hub/
	
	auth_url = https://sso.redhat.com/auth/realms/redhat-external/protocol/openid-connect/token
	
	token = SE OBTIENE DESDE https://console.redhat.com/ansible/automation-hub/token
4. Instalación de collections a elección 

4.1. Install collection redhat.openshift

	$ ansible-galaxy collection install redhat.openshift
	
4.2. Install collection community.okd

	$ ansible-galaxy collection install community.okd
	
5. Crear playbook

6. Ejecutar
