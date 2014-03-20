# Ansible Role: Drush

Installs Drush, a command line shell and scripting interface for Drupal, on any Linux or UNIX system.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `vars/main.yml`):

    drush_install_path: /usr/local/share/drush

The location of the entire drush installation (includes all the supporting files, as well as the `drush` executable file.

    drush_path: /usr/local/bin/drush

The path where composer will be installed and available to your system. Should be in your user's `$PATH` so you can run commands simply with `composer` instead of the full path.

This role also relies on the presence of the `composer_path` variable, which is used to run composer. This could be, simply, `composer` on your system (if composer is in your user's `$PATH`).

    drush_version: master

The version of Drush to install (examples: `master` for the bleeding edge, `7.x`, `6.x`, `6.2.0`).

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

This role was created in 2014 by Jeff Geerling (@geerlingguy), author of Ansible for DevOps. You can find out more about the book at http://ansiblefordevops.com/, and learn about the author at http://jeffgeerling.com/.
