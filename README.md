# Ansible Role: PHP PECL 
[![Build Status](https://travis-ci.org/darthwade/ansible-role-php-pecl.png)](https://travis-ci.org/darthwade/ansible-role-php-pecl)
[![Gittip](http://img.shields.io/gittip/darthwade.svg)](https://www.gittip.com/darthwade/)

Ansible role that installs PHP PECL and its extensions.

Features include:
- Installation of PHP PECL and it's dependencies
- Basic configuration
- Installation of PHP PECL extensions

## Installation

Using `ansible-galaxy`:
```shell 
$ ansible-galaxy install darthwade.php-pecl
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):
```shell 
$ arm install darthwade.php-pecl
```

Using `git`:
```shell 
$ git clone https://github.com/darthwade/ansible-role-php-pecl.git
```

## Requirements & Dependencies
- Ansible 1.4 or higher
- PHP
- PHP PEAR

## Variables
Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```yaml
# A list of extensions that should be installed via pecl install.
php_pecl_extensions:
  - xdebug
  - opcache
```

## Example playbook
```yaml
- hosts: all
  vars:
    php_pecl_extensions:
    - xdebug
    - zendopcache
  roles:
    - darthwade.php-pecl
```

## Testing
```shell 
$ git clone https://github.com/darthwade/ansible-role-php-pecl.git
$ cd ansible-role-php-pecl
$ vagrant up
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License

Licensed under the MIT License. See the LICENSE file for details.

Copyright (c) 2014 [Vadym Petrychenko](http://petrychenko.com/)