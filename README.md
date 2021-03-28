# Ansible Role: PHP-MySQL

Installs PHP [MySQL](https://www.mysql.com/) support on Linux.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    php_enablerepo: ""

(RedHat/CentOS only) If you have enabled any additional repositories (might I suggest sbalandine.repo-epel or sbalandine.repo-remi), those repositories can be listed under this variable (e.g. `remi,epel`). This can allow you to install later versions of PHP packages.

    php_mysql_package: php-mysql # RedHat
    php_mysql_package: php5-mysql # Debian

The PHP MySQL package to install via apt/yum. This should only be overridden if you need to install a unique/special package for MySQL support, as in the case of using software collections on Enterprise Linux.

## Dependencies

  - sbalandine.php

## Example Playbook

    - hosts: webservers
      roles:
        - { role: sbalandine.php-mysql }

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/) and adapted by Serge Balandine.

