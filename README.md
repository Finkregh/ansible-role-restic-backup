restic-backup
=========

Install and configure https://github.com/binarybucks/restic-tools to do backups with restic

Requirements
------------

- systemd

Role Variables
--------------

You can configure all backends that resitc supports (https://restic.readthedocs.io/en/latest/030_preparing_a_new_repo.html), just set the variables in the following list.
You can also have multiple `backup_destinations`.

```yaml
backup_destinations:
  - name: b2-example # 
    RESTIC_REPOSITORY: 'b2:something:something/'
    B2_ACCOUNT_ID: 'account-id'
    B2_ACCOUNT_KEY: 'account-key'
    RESTIC_PASSWORD: 'generated'
```

Some more settings from https://github.com/binarybucks/restic-tools, the `local.config` part
```yaml
restic_local_config:
  BACKUP_HOSTNAME: '{{ inventory_hostname }}'
  BACKUP_DIR: '/'
  HEALTHCHECK_URL: ''
```

Dependencies
------------

-/-

Example Playbook
----------------

FIXME

License
-------

BSD

Author Information
------------------

Oluf Lorenzen, https://mafia-server.net
