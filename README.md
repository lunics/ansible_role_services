# Ansible role: SERVICES

```yaml
systemd_services:
  - name:        my_service_name        # required
    state:       started                # optional, default=started
    enabled:     true                   # optional, default=true
    description: Just a description
    type:        simple                 # required
    environments:
      - WAYLAND_DISPLAY=wayland-1
      - XDG_RUNTIME_DIR=/run/user/%i
    exec_start:  /path/my_script.sh
```

## Todo
- loop sur les ExecStart
