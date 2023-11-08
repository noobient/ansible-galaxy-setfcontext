# noobient.setfcontext

## Synopsys

This role lets you set the SELinux fcontext for the given pattern and apply it to the given path.

## Parameters

| Name | Required | Example | Description |
|---|---|---|---|
| `path` | yes | `/var/www/db` | Path to run `restorecon` on after setting up the fcontext. |
| `type` | yes | `httpd_sys_rw_content_t` | fcontext type to set for the given pattern. |
| `pattern` | yes | `/var/www/db(/.*)?` | Pattern that corresponds to the given type. |

## Examples

```yml
- include_role:
    name: noobient.setfcontext
  vars:
    path: '/var/www/db'
    type: 'httpd_sys_rw_content_t'
    pattern: "/var/www/db(/.*)?"
```

## Return Values

N/A

## Support

| Platform | Support | Status |
|---|---|---|
| Linter | ✅ | [![Lint](https://github.com/noobient/ansible-galaxy-setfcontext/actions/workflows/lint.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-setfcontext/actions/workflows/lint.yml) |
| AlmaLinux 8 | ✅ | [![AlmaLinux 8](https://github.com/noobient/ansible-galaxy-setfcontext/actions/workflows/almalinux-8.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-setfcontext/actions/workflows/almalinux-8.yml) |
| AlmaLinux 9 | ✅ | [![AlmaLinux 9](https://github.com/noobient/ansible-galaxy-setfcontext/actions/workflows/almalinux-9.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-setfcontext/actions/workflows/almalinux-9.yml) |
| Fedora 38 | ✅ | [![Fedora 38](https://github.com/noobient/ansible-galaxy-setfcontext/actions/workflows/fedora-38.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-setfcontext/actions/workflows/fedora-38.yml) |
| Fedora 39 | ✅ | [![Fedora 39](https://github.com/noobient/ansible-galaxy-firewalld/actions/workflows/fedora-39.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-firewalld/actions/workflows/fedora-39.yml) |
| Ubuntu 18.04 | ❌ | N/A |
| Ubuntu 20.04 | ❌ | N/A |
| Ubuntu 22.04 | ❌ | N/A |
