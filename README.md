UPD This repository is fork from https://github.com/skysider/pwndocker
README is changed in part of docker using

Original README
Pwndocker
=========
A docker environment for pwn in ctf based on **skysider/pwndocker:latest**

### Usage

	docker run -d \
		--rm \
		-h ${ctf_name} \
		--name ${ctf_name} \
                --user $(id -u):$(id -g) \
		-v $(pwd)/${ctf_name}:/ctf/work \
		-p 23946:23946 \
		--cap-add=SYS_PTRACE \
		luckycatalex/pwndocker
	
	docker exec -it ${ctf_name} /bin/bash

This image just adds ability of working from non-root user
