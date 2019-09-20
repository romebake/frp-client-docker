# Frp Client Docker

## Example Usage

1.Create **frpc.ini** file in the **/home/frpc** directory

```ini
[common]
server_addr = test.com
server_port = 7788

[secret_ssh_visitor]
type = stcp
role = visitor
server_name = secret_ssh
sk = test
bind_addr = 127.0.0.1
bind_port = 3000
```

2.Create docker container

```bash
docker run -d --name frpc --net host -v /home/frpc/frpc.ini:/frp/frpc.ini --restart=always romebake/frp-client:latest
```

---

## Others

[frp-server-docker](https://github.com/romebake/frp-server-docker)
