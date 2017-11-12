pyslackers.letsencrypt
======================

Ansible role to generate letsencrypt certificates.

Role Variables
--------------

* `domain`: List of domains name for this certificate.
* `email`: Email address for letsencrypt notifications.
* `webserver`: Webserver service to stop when generating certificates for the first time.
* `certbot_port`: Listening port for certbot during certificates renewal (default to `32456`).

Example Playbook
----------------

```yml
- hosts: localhost
  vars:
    webserver: haproxy
    email: noreply@example.com
    domains: 
        - ansible.example.com
  roles: 
    - pyslackers.letsencrypt
```

License
-------

MIT
