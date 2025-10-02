# dashy-podman
Run dashy with Quadlet in Podman

If `$HOME/.config/containers/systemd/` doesn't exists , create it
```
mkdir -p $HOME/.config/containers/systemd/
```

Put `dashy.container` in `$HOME/.config/containers/systemd/`

Inform systemd of the dashy.container configuration
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
