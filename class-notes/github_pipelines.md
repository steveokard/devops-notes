# Github Action Pipelines

when deploying find the docker image name and tag to use.
Kubernetes is the orchestration of docker images providing the automation of deployment for containers in a highly available way (etc)

## Docker Considerations
today's example is going to be: `docker pull linuxserver/plex:latest`

**remember when using the latest image, there might be changes made at any time that can cause conflicts and break things. maybe you should specify a specific version instead!**

### Docker Commands & Variables
_you should look for docker environment variables or even a docker command with parameters to use_

* -e parameter is environment variables
* -v parameter refers to volumes to mount in the container
* -p parameter is for ports to expose/open into the container

For plex they mention you should mount the locations of your movies folder, your tv series folder, and _a folder to mount for your plex configuration_

## Vaas Repo
pipeline = .github folder
manifests folder = manifests
library folder is organized by technology

* Clone a manifest and vars for plex
* in docker file, specify the image name
    * `IMAGE linuxserver/plex:latest`
customize the templates for your needs.

## GitHub Pipelines
**when you set up a technology for the _first_ time, you need to merge your branch into master/main so github knows to set up a pipeline for it**

