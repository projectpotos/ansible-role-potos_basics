# Ansible Role - Potos Basics

Role to manage the basic Potos Linux Client functionallity like hourly ansible pull

[![Test](https://github.com/projectpotos/ansible-role-potos_basics/actions/workflows/test.yml/badge.svg)](https://github.com/projectpotos/ansible-role-potos_basics/actions/workflows/test.yml)

# Role Variables

* `potos_basics_ansible_workdir`: Location for the ansible to execute, by default at "/var/lib/{{ client_name | lower }}/ansible"
* `potos_basics_ansible_logdir`: Log directory for the ansible runs, by default "/var/log/{{ client_name | lower }}"
* `potos_basics_playbook_version`: Which version of the potos playbook should be used, by default 'main'
* `potos_basics_ansible_inventory`: Location of the ansible inventory file, by default "/etc/ansible/inventory/{{ client_name | lower }}_inventory"
* `potos_basics_runtypes`: List of available runtypes, by default 'setup', 'daily' and 'hourly'
* `potos_basics_on_error_additional_lines`: List of lines to be added to message on ansible error
* `potos_basics_enable_reboot_reminder`: If users should be reminded to restart their machine after {{ potos_basics_reboot_reminder_days }} days of uptime, by default yes
* `potos_basics_reboot_reminder_days`: How many days should pass until a user is reminded to restart, by default 10

# Dependencies

As the basic role of [Potos Linux Client](https://potos.dev) this role has a dependency on the global variables of a Potos Linux Client and expects to be executed with the [Potos Playbook](https://github.com/projectpotos/ansible-plays-potos).
