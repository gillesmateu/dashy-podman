# dashy-podman
## Run Dashy (https://dashy.to/) with Quadlet in Podman

If `$HOME/.config/containers/systemd/` doesn't exists , create it
```
mkdir -p $HOME/.config/containers/systemd/
```

Upgrade `dashy.container` with your settings and put it in `$HOME/.config/containers/systemd/`

You can put a sample configuration file in the data directory you informed in `dashy.container` or start without configuration.
Sample condiguration files can be found here: https://gist.github.com/Lissy93/000f712a5ce98f212817d20bc16bab10

Inform systemd of the `dashy.container` configuration
```
$ systemctl --user daemon-reload
```

Start the service
```
$ systemctl --user start dashy.service
```

Check the status
```
$ systemctl --user status dashy.service
● dashy.service
     Loaded: loaded (/home/gmateu/.config/containers/systemd/dashy.container; generated)
     Active: active (running) since Thu 2025-10-02 11:07:58 CEST; 4s ago
     ...
```

Browse to your Dashy url, ex: http://127.0.0.1:8080/

## Usefull links:
- Dashy: https://dashy.to
- Podman: https://podman.io
- Podman Quadlet: https://docs.podman.io/en/latest/markdown/podman-systemd.unit.5.html
- Podman Desktop: https://podman-desktop.io
