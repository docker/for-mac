## Docker for Mac

### Getting Docker for Mac

Docker for Mac is free to [download](https://www.docker.com/products/docker#/mac).

### Documentation

If you don't understand something about Docker for Mac, the [extensive
documentation](https://docs.docker.com/docker-for-mac/) is a great place
to look for answers.

### Support

Users from the Docker community trade tips and tricks and discuss Docker
for Mac in [the user forum](https://forums.docker.com/c/docker-for-mac).

Problems with the Docker for Mac software can be filed as issues in this
([docker/for-mac](https://github.com/docker/for-mac)) repository.

### This Repository

This repository contains an issue tracker for Docker for Mac -- an
integrated Docker experience on OS X or macOS. If you find a problem
with the software, first [browse the existing
issues](https://github.com/docker/for-mac/issues) or search from the bar
at the top (`s` to focus) and then, if you don't find your issue, [open
a new issue](https://github.com/docker/for-mac/issues/new).

### Labels

Initially, issues are
[unlabeled](https://github.com/docker/for-mac/issues?q=is%3Aopen+is%3Aissue+no%3Alabel). Issues
are labeled in order to make tracking them easier. The meaning of the
labels is roughly:

| Label            | Meaning                                            |
|------------------|----------------------------------------------------|
| [area/compose](https://github.com/docker/for-mac/labels/area/compose)     | related to [docker/compose](https://github.com/docker/compose) |
| [area/docker](https://github.com/docker/for-mac/labels/area/docker)      | related to the Docker engine ([docker/docker](https://github.com/docker/docker)) |
| [area/gui](https://github.com/docker/for-mac/labels/area/gui)         | related to the Graphical User Interface |
| [area/linux](https://github.com/docker/for-mac/labels/area/linux)       | related to the Linux component |
| [area/mounts](https://github.com/docker/for-mac/labels/area/mounts)      | related to `-v` bind mounts |
| [area/network](https://github.com/docker/for-mac/labels/area/network)     | related to container networking |
| [area/notary](https://github.com/docker/for-mac/labels/area/notary)      | related to [docker/notary](https://github.com/docker/notary) |
| [area/osx](https://github.com/docker/for-mac/labels/area/osx)         | related to OS X or macOS integration |
| [area/startup](https://github.com/docker/for-mac/labels/area/startup)     | related to application installation or initialization |
| [area/storage](https://github.com/docker/for-mac/labels/area/storage)     | related to image and container storage ([storage drivers](https://docs.docker.com/engine/userguide/storagedriver/imagesandcontainers/)) |
| [area/volumes](https://github.com/docker/for-mac/labels/area/volumes)     | related to Docker volumes ([volume drivers](https://docs.docker.com/engine/reference/commandline/volume_create/)) |
| [kind/bug](https://github.com/docker/for-mac/labels/kind/bug)         | this issue describes a defect |
| [kind/docs](https://github.com/docker/for-mac/labels/kind/docs)        | this issue describes a documentation change |
| [kind/enhancement](https://github.com/docker/for-mac/labels/kind/enhancement) | this issue describes a change to existing functionality |
| [kind/feature](https://github.com/docker/for-mac/labels/kind/feature)     | this issue describes totally new functionality |
| [kind/performance](https://github.com/docker/for-mac/labels/kind/performance) | this issue describes a performance problem or measurement |

### Component Projects

Docker for Mac uses many open source components. A full list of
components and licenses is available inside of Docker from `About Docker
-> Acknowledgements` in the :whale: menu.

Some notable components include:

 * [HyperKit](https://github.com/docker/hyperkit/), a toolkit for
   embedding hypervisor capabilities in your application
 * [DataKit](https://github.com/docker/hyperkit/), a tool to orchestrate
   applications using a 9P dataflow
 * [VPNKit](https://github.com/docker/vpnkit), a set of tools and
   services for helping HyperKit VMs interoperate with host VPN
   configurations
