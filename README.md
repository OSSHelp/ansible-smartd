# smartd

[![Build Status](https://drone.osshelp.ru/api/badges/ansible/smartd/status.svg)](https://drone.osshelp.ru/ansible/smartd)

Installs smartd plus minimal configuration

## Usage (example)

```yaml
    - role: smartd
```

## Available parameters

| Param | Default | Description |
| -------- | -------- | -------- |
| `smartd_setup` | `full` | Setup mode. See [OSSHelp KB article](https://oss.help/kb4895) |
| `smartd_role_test_mode` | `false` | Param to properly test role in builds, do not use it in playbooks. |
| `email_to` | `root` | User to whom the message will be sent |
| `smartd_test_alert` | `true` | Parameter to control the sending of a test alert |
| `dev_type` | `` | Specifies the type of the device. See -d option in the [man 5 smartd.conf](https://linux.die.net/man/5/smartd.conf). |
| `smartd_devices_to_ignore` | `[]` | List of devices to ignore |

## FAQ

...

## Useful links

- [Official documentation](https://www.smartmontools.org/wiki/TocDoc)

## TODO

- NVMe devices support?

## License

GPL3

## Author

OSSHelp Team, see <https://oss.help>
