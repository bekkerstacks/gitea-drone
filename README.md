# gitea-drone
Gitea and Drone-CI

## Example Pipeline

- `.drone.yml`

```
kind: pipeline
name: default

steps:
  - name: frontend
    image: alpine
    group: build
    commands:
      - echo hello frontend
      - echo $$HOSTNAME

  - name: backend
    image: alpine
    group: build
    commands:
      - echo hello backend
      - echo $$HOSTNAME
```
