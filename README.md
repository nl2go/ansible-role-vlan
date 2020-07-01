[![Build Status](https://travis-ci.org/nl2go/ansible-role-vlan.svg?branch=master)](https://travis-ci.org/nl2go/ansible-role-vlan)
[![Ansible Galaxy](https://img.shields.io/badge/role-nl2go.vlan-blue.svg)](https://galaxy.ansible.com/nl2go/vlan/)
[![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/nl2go/ansible-role-vlan)](https://galaxy.ansible.com/nl2go/vlan)
[![Ansible Galaxy Downloads](https://img.shields.io/ansible/role/d/49554.svg?color=blue)](https://galaxy.ansible.com/nl2go/vlan/)

# Ansible Role: VLAN

An Ansible Role that manages setup and configuration of an [Open vSwitch](https://www.openvswitch.org/) based VLAN.

## Role Variables

Available variables listed below, along with default values (see `defaults/main.yml`):

    vlan_group: all
    
Host group the VLAN configuration should be applied to.    
    
    vlan_ip: 172.0.0.1

Host IP within the VLAN.    
    
    vlan_interface: vlan0
    
VLAN interface name.    
    
    vlan_netmask: 255.255.255.0
    
VLAN subnet netmask.    
    
    vlan_transport_interface: "{{ ansible_default_ipv4.interface }}"

VLAN physical transport interface.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - nl2go.vlan

## Development

Use [docker-molecule](https://github.com/nl2go/docker-molecule) following the instructions to run [Molecule](https://molecule.readthedocs.io/en/stable/)
or install [Molecule](https://molecule.readthedocs.io/en/stable/) locally (not recommended, version conflicts might appear).

Provide Hetzner Cloud token:

    export HCLOUD_TOKEN=123abc456efg

Use following to run tests:

    molecule test --all

## Maintainers

- [build-failure](https://github.com/build-failure)

## License

See the [LICENSE.md](LICENSE.md) file for details.

## Author Information

This role was created in 2020 by [nl2go](https://github.com/nl2go) team.
