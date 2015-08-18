# Ansible Role: Drush

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-drush.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-drush)

Installs Drush, a command line shell and scripting interface for Drupal, on any Linux or UNIX system.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    drush_install_path: /usr/local/share/drush

The location of the entire drush installation (includes all the supporting files, as well as the `drush` executable file.

    drush_path: /usr/local/bin/drush

The path where drush will be installed and available to your system. Should be in your user's `$PATH` so you can run commands simply with `drush` instead of the full path.

    drush_version: master

The version of Drush to install (examples: `master` for the bleeding edge, `7.x`, `6.x`, `6.2.0`).

    drush_keep_updated: no

Whether to keep Drush up-to-date with the latest revision of the branch specified by `drush_version`.

    drush_clone_depth: ~

Whether to clone the entire repo (by default), or specify the number of previous commits for a smaller and faster clone.

## Dependencies

  - geerlingguy.git (Installs Git).
  - geerlingguy.php (Installs PHP).
  - geerlingguy.composer (Installs Composer).

## Example Playbook

    - hosts: servers
      roles:
        - { role: geerlingguy.drush }

After the playbook runs, the `drush` command will be accessible from normal system accounts.

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/).
