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
| `email_to` | `''` | User or email addr for alert messages |
| `smartd_test_alert` | `true` | Parameter to control the sending of a test alert |
| `smartd_devices_types` | `[sat, scsi, nvme]` | Specifies the devices types list for DEVICESCAN directive. See -d option in the [man 5 smartd.conf](https://linux.die.net/man/5/smartd.conf). |
| `smartd_devices_verify` | `true` | If set to `true` - will try to verify given `smartd_devices_types` with check output of `smartctl -d <type> --scan` for each type and filter out the missing ones. If set to `false` - will use `smartd_devices_types` as is. |
| `smartd_devices_to_ignore` | `[]` | List of devices to ignore |

## FAQ

...

## Useful links

- [Official documentation](https://www.smartmontools.org/wiki/TocDoc)

## TODO

- Proper tests for `smartd_devices_verify` functionality (not possible with LXC)

## License

GPL3

## Author

OSSHelp Team, see <https://oss.help>
