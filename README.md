ansible-role-php_pecl
=====================

Install PECL extensions for PHP via pecl or apt.

Requirements
------------

PHP must already be installed on the server.

Usage
-----

```yml
- hosts: all
  vars:
    php_pecl_extensions:
      - xdebug
  roles:
    - { role: igor_mukhin.php_pecl }
```
