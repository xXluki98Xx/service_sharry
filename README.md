<!--
Shields
Headers
-->

# Hodgins: sharry Service

A repository, providing an sharry service for Hodgins Server.

## Description

This repository provides an ansible-playbook which will:

- pull the image
- create service folder
- create a systemd service file
- start and enable the systemd service
- open up the firewall

## Requirements

A hodgins server or compatible deployment must be provided.

## Install

Clone the repository next to you existing Hodgins Server code.

```
git clone https://github.com/xXluki98Xx/service_sharry.git
```

Afterwards, you can install the service.

```
ansible-playbook -i <path-to-your-inventory> -k -K -u <hodgins-users> playbooks/service_sharry.yml
```

## Usage

The installation will respond to you with a running sharry service.
Now you can enter the report page:

```
http://hodgins-ip:8080/app
```

To interact with the container, you will have multiple options.

Via Systemd on your hodgins server (recommended), you can interact with the service
the same way you are interacting with other services on your system.

Get the status:

```
$ sudo systemctl status podman
```

Restart the service (and apply updated images):

```
$ sudo systemctl restart container_sharry
```

Services in Hodgins are running in containers. You can interact with the containers
via Podman.

Check all containers:

```
podman ps
```

Restart a running container:

```
podman container restart service_sharry
```

## Changelog

The repository contains a curated, chronological [changelog](CHANGELOG.md),
maintained by the owner for each release/tag.

## Contribute

Thank you so much for considering to contribute! We are happy, when someone is
joining the hard work. Please feel free to contribute, after having a look at
the [Conventions](https://github.com/while-true-do/doc-library/).

- [Bugs and Feature Requests](https://github.com/xXluki98Xx/sharry/issues)
- [Pull Requests](https://github.com/xXluki98Xx/service_sharry/pulls)

See who has contributed already in the [KUDOS.txt](KUDOS.txt).

## Test

tbd

## License

This work is [licensed](LICENSE) under a
[BSD-3-Clause License](https://opensource.org/licenses/BSD-3-Clause).

## Contact

-   Site <https://while-true-do.io>
-   Code <https://github.com/while-true-do>
-   Mail [hello@while-true-do.io](mailto:hello@while-true-do.io)
-   Chat [@freenode #while-true-do](https://webchat.freenode.net/#while-true-do)
