# Ansible Playbooks Lab

Dit is een oefenproject waarin ik Ansible gebruik op localhost met een `common` rol.

## Mappenstructuur

- `inventory/hosts.ini` – Inventory bestand met localhost
- `playbooks/localtest.yml` – Playbook dat de `common` rol aanroept
- `roles/common/` – Een rol met taken, handlers, templates, enz.

## Uitvoeren

```bash
ansible-playbook -i inventory/hosts.ini playbooks/localtest.yml
