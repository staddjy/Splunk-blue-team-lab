```

- **sysmon-config.xml**: Sysmon rule set used to log key events like process creation, network connections, logons, etc.
- **inputs.conf**: Tells Splunk Universal Forwarder which logs to collect (Security logs and Sysmon events).
- **outputs.conf**: Sends collected logs to the Splunk Enterprise server running on Ubuntu (10.128.0.2:9997).
