[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border.json)](https://github.com/copier-org/copier)
[![Podman Badge](https://img.shields.io/badge/Podman-892CA0?logo=podman&logoColor=white)](https://podman.io/)
[![Hatch project](https://img.shields.io/badge/%F0%9F%A5%9A-Hatch-4051b5.svg)](https://github.com/pypa/hatch)
![CI](https://github.com/ansible-selfhosted/selfhosted.services.readarr/actions/workflows/ci.yml/badge.svg)
[![Ansible](https://img.shields.io/badge/Ansible-Molecule-EE0000?style=plastic&logo=ansible&logoColor=white)](https://github.com/ansible/molecule)

<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: [readarr](https://wiki.servarr.com/en/readarr)

A role to deploy Readarr using rootless Podman with systemd.

## Role Requirements

- none

*Refer to services collection for general requirements*

## Role Arguments

|Option|Description|Type|Required|Default|
|---|---|---|---|---|
|readarr_config_path|The path to the readarr configuration directory|str|False|~/.config/readarr/|
|readarr_data_path|The path to the readarr data directory<br>It is recommended to share the same data directory with other media managing services|str|False|~/.local/share/containers/storage/media|
|readarr_timezone|The timezone for the readarr service|str|False|Etc/UTC|
|readarr_web_port|The port for the web server|int|False|8787|


## Example Playbook

```
- hosts: all
  tasks:
    - name: Importing readarr role
      ansible.builtin.import_role:
        name: selfhosted.services.readarr
      vars:
```

## License

This project is licensed under the [MIT License](LICENSE)


⊂(▀¯▀⊂)

<!-- END_ANSIBLE_DOCS -->
