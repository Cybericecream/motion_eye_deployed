# Welcome to the Motion Eye Deployed
This was built to be used on a Intel NUC, at initial testing on a cheap Intel i3 NUC I estimate you can hold 12-15 consistent streams at 720p.
### Index
- [Updates](/docs/updates)
- [Networking](/docs/network)

### Links

#### Motion Eye
Motion Eye is on the root point.<br />
[Links to Motion Eye](/)

#### Docs
The Docs are on the end point `/docs`<br />
[Links to Docs](/docs)

## Tech Stack
- Ubuntu
    - Zsh Terminal
      - Oh My Zsh
    - Docker / Docker Compose
      - Nginx
      - Motion Eye
      - Material MkDocs

## Simple Trouble Shooting
I don't expect there to be regular issue however if there is follow the following steps. Obviously simply try turning it on and off again.

#### Reboot Ubuntu Once Connected Via SSH
To reboot ubuntu you need to run the shutdown command as root (sudo) with the flag `-r` or restart.
```bash
sudo shutdown -r
```

#### 1. Connect and Route
Connect to the box via SSH once tou have simply route to the project files found at `/srv/motion_eye_deployed` then run the following;
```bash
cd /srv/motion_eye_deployed
```

#### 2. Reboot the containers
Once at the project files reboot the docker containers
```bash
docker-compose down; docker-compose up
```