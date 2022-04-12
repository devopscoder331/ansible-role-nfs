Role Name
=========

This role install and configure NFS server. This role has been developed to be used in the my projects.

Requirements
------------

None

Role Variables
--------------

* `nfs_exports`: List of dictionaries of NFS shares
  * `path`: Shared directories to export
  * `acls`: List of clients with options

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - role: username.rolename
          nfs_exports:
          - path: "/var/nfs/folder1"
            acls: 
              - 192.168.1.0/24(rw,sync,subtree_check)

Example Client
----------------

Mount NFS shares on client as shown below:

```
sudo mount -t nfs -vvvv -o vers=4 xx.xx.xx.xx:/var/nfs/folder1 /home/user/folder1
```

Dependencies
------------

None.


License
-------

MIT

Author Information
------------------

This role was created in 2022 by @devopscoder331.
