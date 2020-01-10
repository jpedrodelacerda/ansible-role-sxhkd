sxhkd role
=========

Installation and configuration of sxhkd.

Requirements
------------

- ArchLinux
- [Ansible AUR](https://github.com/kewlfft/ansible-aur)

Role Variables
--------------

This role contains only `sxhkd_bindings` dictionary.
The bindings have the following structure:
```
- name:
  binding:
  exec:
```
> The name attribute is optional.

Example:
```
sxhkd_bindings:
  - name: Launch Tilix
    binding: super + Return
	exec: tilix
```

```
# cat $HOME/.config/sxhkd/sxhkdrc
# Launch Tilix
super + Return
        tilix

```

Dependencies
------------

None.

Example Playbook
----------------

```
    - hosts: localhost
      roles:
         - { role: jpedrodelacerda.sxhkd }
```

License
-------

MIT
