# Ansible tetsensor
Basic Ansible script to remove any existing Tetration sensor and install a new version including the dependencies.

## Configuration
In `group_vars/all` you will find variables that need to be configured.

```
http_proxy: http://myproxy.company.com:80
no_proxy: "127.0.0.1,localhost"
sensor_file: /tmp/sensor.rpm
```

Proxy is only required if you dependencies need access to a public repository and that you need to use a proxy.

`sensor_file` is the location of the sensor file to deploy on the VM.

## Usage
`ansible-playbook tetration.yml -u ansible --private-key=ssh/ansible-ssh -i inventory_location`
