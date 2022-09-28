Ansible Prometheus + Grafana + Node Exporter
===

Example taken from: https://github.com/prometheus/demo-site

How to Use
---
1. Install dependencies
```bash
# Download roles
ansible-galaxy install -r requirements.yml
```
2. Add Remote IP to `hosts`

3. Add Grafana Password
```bash
# create new vault
ansible-vault create --vault-id @prompt vault
```

    with content

```
vault_grafana_password: <<INSERT_YOUR_GRAFANA_PASSWORD>>
```

4. Run Ansible Playbook
```bash
# Run playbook
ansible-playbook -i hosts deploy.yml

# or when using vault encrypted variables
ansible-playbook -i hosts --vault-id @prompt deploy.yml
```
