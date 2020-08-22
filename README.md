# getting_started
Here some resources to help get started

## Install Docker
https://docs.docker.com/get-docker/

## Install VSCode
https://code.visualstudio.com/

## Clone Repo and Run

Run `git clone https://github.com/Pitt-Cyber-Security/getting_started.git` in whatever directory you want to work in. Then run the bash `build.sh` and `run.sh` scripts in the directory to start getting to work.

### Don't have git installed

Created a new folder with three files
* Dockerfile
* build.sh
* run.sh

### Can't run bash scripts

Bash scripts are UNIX dependent so as long as you have docker installed you can run to build:
```
docker build . -t pitt_ctf
```

and to run:

```
docker run -it -e "TERM=xterm-256color" --privileged --cap-add=SYS_PTRACE --security-opt seccomp=unconfined -v "$(pwd)/":/root/ctfs pitt_ctf /bin/bash
```

*Note* If you have a windows machine you may need to run these commands in PowerShell to get it to work.
