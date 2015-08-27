CIS
=========

This role can be used to audit or remediate a host against the Center for Internet Security (CIS) security benchmarks.

*Disclaimer: This project has no affiliation with CIS.  The role and its contents have not been reviewed or endorsed by CIS.*

Requirements
------------

This role has no requirements or dependencies.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

Some sensible defaults are configured and documented within defaults/main.yml.  These defaults are set so they would cause minimal disruption to a production system.  However, it's *your* responsibility to verify that the default configuration will not harm your production server.  *Always* run the role in check mode if you're unsure of its effects.

Be aware that some of the default variables are set against CIS recommendations in the hopes that they will cause minimal disruption to a system.

Example Playbook
----------------

Playbooks can utilize the CIS role without much effort:

    - hosts: all
      roles:
        - cis 

The role is thoroughly tagged so that you can run certain sections or certain levels of checks:

    # Test only items from section 4
    ansible-playbook -i hosts -C playbook.yml -t section4

    # Apply changes only from items in section 4, 5, and 6
    ansible-playbook -i hosts playbook.yml -t section4,section5,section6

License
-------

Apache License, Version 2.0

Author Information
------------------

Major Hayden <major@mhtx.net>
