# Ansible Role for Papertrails RemoteSyslog2

[![Build Status](https://travis-ci.org/mortik/ansible-remote-syslog.png?branch=master)](https://travis-ci.org/mortik/ansible-remote-syslog)

A Simple Role to install Remote Syslog 2

## Role Variables

```yaml
remote_syslog_package_url: https://github.com/papertrail/remote_syslog2/releases/download/v0.13/remote_syslog_linux_amd64.tar.gz
remote_syslog_files: []
remote_syslog_host: logs.papertrailapp.com
remote_syslog_port: 1234
remote_syslog_protocol: tls
```

## License

MIT

