# Ansible Nginx Practice Task

This playbook installs Nginx, deploys a simple HTML page, and ensures the service is running.

## ✅ Steps

1. Test connection:
   ```bash
   ansible -i inventory.ini webservers -m ping

2. Run playbook:
   ```bash
   ansible-playbook -i inventory.ini site.yml

3. Run again (should report changed=0):
    ```bash
   ansible-playbook -i inventory.ini site.yml

4. Verify in browser or via curl:
      ```bash
   curl http://SERVER_IP/
