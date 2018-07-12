# drone-dingtalk

Drone plugin for sending dingtalk notifications.

```
pipeline:
  dingtalk:
    image: xtony77/drone-dingtalk
    webhook: https://oapi.dingtalk.com/robot...
    when: 
      status: [ failure, success ]
```

Example configuration with custom secrets:

```
pipeline:
  dingtalk:
    image: xtony77/drone-dingtalk
    secrets:
      - source: ${custom_secret_name}
        target: plugin_webhook
    when:
      status: [ failure, success ]
```

