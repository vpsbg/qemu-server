# qemu-server

This fork currently carries one change: support multiple IPv4 and IPv6 addresses per Cloud-Init `ipconfigN` interface using semicolon-delimited lists.

Branch:

- `ipconfig-multi-address-9.1.6` for `qemu-server 9.1.6`

Apply:

1. Check out branch `ipconfig-multi-address-9.1.6`.
2. Copy `src/PVE/QemuServer/Network.pm` to `/usr/share/perl5/PVE/QemuServer/Network.pm`.
3. Copy `src/PVE/QemuServer/Cloudinit.pm` to `/usr/share/perl5/PVE/QemuServer/Cloudinit.pm`.
4. Run:

```bash
systemctl restart pvedaemon pveproxy
```
