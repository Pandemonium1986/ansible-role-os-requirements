# Ansible role : OpenStack Requirements

![Ansible Role](https://img.shields.io/ansible/role/46372?logo=ansible)
![Gitlab pipeline status](https://img.shields.io/gitlab/pipeline/Pandemonium1986/ansible-role-os-requirements?logo=gitlab)
![GitHub release](https://img.shields.io/github/release/Pandemonium1986/ansible-role-os-requirements.svg?logo=github)
![Github license](https://img.shields.io/github/license/Pandemonium1986/ansible-role-os-requirements.svg?logo=github)
![Ansible Quality Score](https://img.shields.io/ansible/quality/46372?logo=ansible)

Install and check if OpenStack requirements are available on control node.

## Disclaimer

!!! This images is no longer support.!!!

## Requirements

This role is not self contained. He requires pandemonium1986.pip to work correctly.

```sh
  ansible-galaxy install -f pandemonium1986.pip
```

## Role Variables

From defaults/main.yml :

```yaml
osrequirements_users:
  - pandemonium
osrequirements_oscli_config_file: "~/.config/openstack/clouds.yaml"
```

## Dependencies

-   pandemonium1986.pip

## Example Playbook

```yaml
- name :                        Openstack deployement
  hosts:                        local
  become:                       true
  tasks:
    - import_role:
        name:                   pandemonium1986.os_requirements   
```

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details

## Author Information

-   **Michael Maffait** - _Initial work_ - [Pandemonium1986](https://github.com/Pandemonium1986)
