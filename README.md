Ansible Role: actrunner
=========

Installs Gitea Act Runner on Linux machines.

Install
-------
Using ansible galaxy

`ansible-galaxy install bcook254.actrunner`

Requirements
------------

Permission to:
  - Create or modify users/groups
  - Create or modify required directories

Role Variables
--------------
A non-exhuastive list of available variables is listed below, along with their default vaules. For a list of variables available for the Act Runner configuration file, please see `defaults/main.yml`.

    actrunner_version: 0.2.10

The version of Act Runner to be installed.

    actrunner_user: actrunner
    actrunner_group: actrunner

The user and group that will be created and Act Runner will run under.

    actrunner_home_dir: /var/lib/actrunner
    actrunner_data_dir: "{{ actrunner_home_dir }}"
    actrunner_bin_dir: /usr/local/bin
    actrunner_config_dir: /etc/actrunner

Default folders created for Act Runner binaries and data.

    actrunner_bin_file: "{{ actrunner_bin_dir }}/actrunner"
    actrunner_config_file: "{{ actrunner_config_dir }}/config.yaml"

Default file names for the Act Runner binary and config file.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: bcook254.actrunner
           become: yes

License
-------

MIT / BSD

Author Information
------------------

This role was created by Benjamin Cook.
