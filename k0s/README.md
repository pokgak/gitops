# k0s setup

## Issues

### k0sctl apply failed due to SSH host key mismatch

Fix: disable ssh host key checking for Tailscale nodes

```
Host 100.*.*.*
  StrictHostKeyChecking no
```

### machine-id not unique

Cause: cloning disk using proxmox
Fix: https://unix.stackexchange.com/a/403054
