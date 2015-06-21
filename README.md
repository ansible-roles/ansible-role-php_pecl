# ansible-role-php_pecl

Install PECL extensions for PHP via pecl or apt.

## Requirements

PHP must already be installed on the server.

## Usage

```yml
- hosts: all
  vars:
    php_pecl_extensions:
      - xdebug
  roles:
    - { role: igor_mukhin.php_pecl }
```

Also, you can install apt packages that do same things:

```yml
- hosts: all
  vars:

  	# Install apt ackages
	php_pecl_apt_packages:
	  - php5-intl
	  - php5-mcrypt

	# And enable it
	php_pecl_modules_enable:
	  - intl
	  - mcrypt

  roles:
    - { role: igor_mukhin.php_pecl }
