# ipf-netbox
Code for IP Fabric and NetBox talk at Cisco Live Amsterdam 2023

1. Clone Git repo
```
git clone https://github.com/richbibby/ipf-netbox.git
cd ipf-netbox
```
2. Create and activate Python 3.10 virtual environment
```
python3.10 -m venv venv
source venv/bin/activate
```
3. Set environment variables for NetBox API token and URL
```
export NETBOX_TOKEN=<token>
export NETBOX_API=<https://url> 
```
4. Install required Python packages
```
pip install -r requirments.txt
```
5. Check Ansible dynamic inventory is working
```
ansible-inventory --list -i netbox_inv.yml
```
6. Run playbook to generate configs
```
ansible-playbook generate_config.yml
```

7. Deactivate virtualenv
```
deactivate
```
