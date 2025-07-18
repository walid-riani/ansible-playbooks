# Ansible Playbooks Lab

Dit is een oefenproject waarin ik Ansible gebruik op `localhost` via een eenvoudige setup met een `common` rol. Het doel is om vertrouwd te raken met het gebruik van Ansible roles, inventories, templates, handlers en playbooks in een gestructureerde directory.

## 🔧 Projectstructuur

ansible-playbooks/
├── ansible.cfg
├── inventory/
│ └── hosts.ini
├── playbooks/
│ └── localtest.yml
├── roles/
│ └── common/
│ ├── defaults/
│ ├── files/
│ ├── handlers/
│ │ └── main.yml
│ ├── tasks/
│ │ └── main.yml
│ ├── templates/
│ └── vars/
├── group_vars/
├── host_vars/
├── templates/
└── README.md

## ⚙️ Uitleg per onderdeel

- **ansible.cfg**: Lokale Ansible-configuratie (indien nodig).
- **inventory/hosts.ini**: Bevat `localhost` als target voor de playbooks.
- **playbooks/localtest.yml**: Playbook dat de `common` rol uitvoert.
- **roles/common/**: Structuur volgens best practices (met onderverdeling in `tasks`, `handlers`, `templates`, etc.).
- **group_vars/ & host_vars/**: Voor variabelen per groep of host.
- **templates/**: Extra globale Jinja2-templates (optioneel).

## ▶️ Uitvoeren

Zorg dat je in de hoofdmap van het project staat (`ansible-playbooks/`) en gebruik:

```bash
ansible-playbook -i inventory/hosts.ini playbooks/localtest.yml
