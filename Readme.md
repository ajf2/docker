# Docker Experiments
This repo is a set of notes and configs/code for the Docker tutorials found at https://docs.docker.com/get-started/.

## About Docker Toolbox
The Docker Desktop tools will only work on 64-bit systems with CPU hardware virtualization and a compatible hypervisor installed. On Windows, this means using an edition that includes Hyper-V.

When running Windows 10 Home, Hyper-V is not available so Docker Desktop won't work. In this situation, use the legacy `Docker Toolbox` instead. Docker Toolbox will also run on Windows 7, which did not have the Hyper-V feature available in any edition.

Docker Toolbox installs VirtualBox and sets up a Docker Machine with that. There are a few extra things to bear in mind.

### Don't try localhost
When following the tutorials, it will mention connecting to `http://localhost:4000` to view the container's ouput. This won't work using Docker Toolbox and instead you must connect to the Docker Machine's IP address instead. Find this with the command
```
$ docker-machine ip
```

### Don't use Edge
Similarly to the above, the Microsoft Edge browser fails to connect even when using the Docker Machine's IP address. Vivaldi works fine, so any Chromium-based browser should also be fine.
