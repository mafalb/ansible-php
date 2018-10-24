
- hosts: ess
  roles:
    - role: scl
    - role: apache/daemon
      apache_scl_prefix: httpd24
      apache_scl_enabled: true

    - role: php/mod_php
      apache_scl_prefix: httpd24
      php_scl_prefix: rh-php70
      php_enabled: false

    - role: php/cli
      php_scl_prefix: rh-php70
      php_enabled: false

    - role: php/mod_php
      apache_scl_prefix: httpd24
      php_scl_prefix: rh-php71
      php_enabled: true

    - role: php/cli
      php_scl_prefix: rh-php71
      php_enabled: true

