## Ansible Nginx Practice Task

This project shows how to use Ansible to set up a simple Nginx web server. 
 
The playbook will:

- Install **nginx** and **curl**
- Ensure `/var/www/html` exists
- Deploy a basic `index.html` page
- Start and enable the nginx service
- Print the final site URL

---

## Files

- **inventory** → Inventory file with server connection details  
- **site.yml** → Main Ansible playbook  
- **ansible.cfg** → Ansible configuration file  
- **Curl output on browser.jpg** → Example proof/screenshot  

---

## Requirements

- Control machine with **Ansible installed**  
- Target host: Ubuntu 20.04/22.04/24.04  
- SSH access with `sudo` privileges  

---

## Run the Playbook

1. Test connection:

   ```bash
   ansible -i inventory webservers -m ping

Run the playbook:
 ```bash
 ansible-playbook -i inventory site.yml

Run again (should show changed=0):
 ```bash
 ansible-playbook -i inventory site.yml


## Verify Deployment
 Browser:
 Open http://<SERVER_IP>/

Curl:
 ```bash
 curl http://<SERVER_IP>/
