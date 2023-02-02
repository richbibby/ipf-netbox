# ipf-netbox
Code for IP Fabric and NetBox talk at Cisco Live Amsterdam 2023. 

The talk demo's the IP Fabric-NetBox plugin to import device data into NetBox, using the NetBox staging functionality. Once the device data has been inmported then the code in this repo demonstrates the following: 

- NetBox as a dyanmic inventory source for Ansible
- Ansible playbook to extract device data from NetBox and render Cisco and Juniper configuration files using Jinja templates

Tested on Python Version: `3.10.6`

1. Clone Git repo and change into ipf-netbox directory
```
git clone https://github.com/richbibby/ipf-netbox.git
cd ipf-netbox
```
2. Create and activate Python 3 virtual environment
```
python3 -m venv venv
source venv/bin/activate
```
3. Set environment variables for NetBox API token and URL
```
export NETBOX_TOKEN=<token>
export NETBOX_API=<https://url> 
```
4. Install required Python packages
```
pip install -r requirements.txt
```
5. Check Ansible dynamic inventory is working
```
ansible-inventory --list -i netbox_inv.yml
```
6. Run playbook to generate configs
```
ansible-playbook generate_config.yml
```

7. Deactivate virtual environment
```
deactivate
```
