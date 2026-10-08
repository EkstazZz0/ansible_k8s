Это учебный теоретический проект по Ansible который настраивает инфраструктуру Kubernetes в следующих условиях:
есть кластер из 7 нод, на которых только установлена ОС Ubuntu Server, заранее создан пользователь ansible, а также установлен и настроен SSH сервер. Необходимо развернуть Kubernetes кластер следующим образом: 3 машины это Control Plane, 2 машины балансировщики для API сервера Control Plane, 2 машины Worker Node. 

ssh ansible client config:

```
Host lb1
    HostName 10.0.0.20
    User ansible
    IdentityFile ~/.ssh/id_ed25519

Host lb2
    HostName 10.0.0.21
    User ansible
    IdentityFile ~/.ssh/id_ed25519

Host cp1
    HostName 10.0.0.11
    User ansible
    IdentityFile ~/.ssh/id_ed25519

Host cp2
    HostName 10.0.0.12
    User ansible
    IdentityFile ~/.ssh/id_ed25519

Host cp3
    HostName 10.0.0.13
    User ansible
    IdentityFile ~/.ssh/id_ed25519

Host worker1
    HostName 10.0.0.31
    User ansible
    IdentityFile ~/.ssh/id_ed25519

Host worker2
    HostName 10.0.0.32
    User ansible
    IdentityFile ~/.ssh/id_ed25519
```
