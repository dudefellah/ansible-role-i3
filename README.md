dudefellah.i3
=========

Install i3 and a configuration file for it.

Requirements
------------

None.

Role Variables
--------------

Variables are defined and described in [defaults/main.yml](defaults/main.yml).
Use of this role should be fairly straight-forward. If you're planning on using
it as an unprivileged user (who can't install system-wide packages), then I
suggest setting `i3_packages` to an empty list (`[]`) to avoid attempts at
performing a priveleged action.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: my_workstations
      tasks:
        - block:
            - name: Run my i3 config
              include_role:
                name: dudefellah.i3
              vars:
                i3_user: bob
                i3_group: bob

License
-------

GPLv2+

Author Information
------------------

Dan - github.com/dudefellah
