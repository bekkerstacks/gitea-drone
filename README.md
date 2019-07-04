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

## Screenshots

Drone-CI:

<img width="1440" alt="image" src="https://user-images.githubusercontent.com/30043398/60689728-c2c34f80-9ec0-11e9-8ed0-be446fbc71fc.png">

Gitea:

<img width="1439" alt="image" src="https://user-images.githubusercontent.com/30043398/60689692-74ae4c00-9ec0-11e9-9b5d-d713c9a86fc1.png">
