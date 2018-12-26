ansible-loggly
==============

Ansible role to forward syslog to Loggly.com

The role also forwards the systemd logs to syslogs as described [here](https://www.loggly.com/docs/systemd-logs/)

Requirements
------------

n/a

Role Variables
--------------

The following role variables are defined as default and can be overriden in the playbook

```yaml
loggly_token:     YOUR_TOKEN_GOES_HERE
loggly_tag:       syslog
loggly_url:       logs-01.loggly.com
loggly_cert:      logs-01.loggly.com_sha12.crt
loggly_cert_path: /etc/rsyslog.d/keys/ca.d
loggly_port:      514
loggly_port_tls:  6514
```

In addition you can set `loggly_tls: true` in order to use [tls configuration](https://www.loggly.com/docs/rsyslog-tls-configuration/) instead of plaintext

Dependencies
------------

n/a

Testing
-------

Assumes you have Ruby and Bundler already installed.

```bash
bundle install  # Only required once
bundle exec kitchen test
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - jmcvetta.loggly

License
-------

This is Free Software, released under the terms of the Apache v2 license.  

Author Information
------------------

[Jason McVetta](mailto:jason.mcvetta@gmail.com)

Paid support and consulting services available from [Silicon
Heavy](http://siliconheavy.com)