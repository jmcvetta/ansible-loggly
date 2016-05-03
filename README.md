ansible-loggly
==============

Ansible role to forward syslog to Loggly.com


Requirements
------------

n/a


Role Variables
--------------

```yaml
loggly_token:  YOUR_TOKEN_GOES_HERE
loggly_tag:    syslog
```


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
