## Debugging
### What can I do to help?
1. First, please refrain from immediately resetting/uninstalling Docker for Mac:
   it will destroy the logs we need to understand the problem.
2. Make sure you are using the latest version of your channel (Stable or Edge).
3. Generate and upload the diagnostics (from the :whale: menu,
   "Diagnose and Feedback")
4. If you are running Stable, consider the possibility of checking whether the
   most recent Edge release addresses your concerns.  Because we continuously
   improve the Diagnostics, it does help us if you can provide Diagnostics with
   the most recent release of Docker for Mac.
5. Check whether there are [open
   issues](https://github.com/docker/for-mac/issues) similar to problem
6. Create a new issue, with a meaningful title, and the Diagnostic ID you
   obtained above, and all the relevant details.

## Versions of Docker for Mac
### Downgrading
There is no GUI interface to install a previous version of Docker for Mac,
however you can still download previous versions from here:

https://docs.docker.com/docker-for-mac/release-notes/

Note the "Download" link for each release.

## Kubernetes
### How can I get logs
```sh
$ docker run --rm -it --privileged --pid=host justincormack/nsenter1 /bin/sh -c "cat /var/log/kubelet.err.log"
```

### getsockopt: connection refused
> When reading `kubelet.err.log` I have tons of:
```
E0131 10:04:34.458760    1193 kubelet_node_status.go:107] Unable to register node "docker-for-desktop" with API server: Post https://192.168.65.3:6443/api/v1/nodes: dial tcp 192.168.65.3:6443: getsockopt: connection refused
E0131 10:04:35.403894    1193 reflector.go:205] k8s.io/kubernetes/pkg/kubelet/config/apiserver.go:47: Failed to list *v1.Pod: Get https://192.168.65.3:6443/api/v1/pods?fieldSelector=spec.nodeName%3Ddocker-for-desktop&resourceVersion=0: dial tcp 192.168.65.3:6443: getsockopt: connection refused
E0131 10:04:35.403894    1193 reflector.go:205] k8s.io/kubernetes/pkg/kubelet/kubelet.go:422: Failed to list *v1.Node: Get https://192.168.65.3:6443/api/v1/nodes?fieldSelector=metadata.name%3Ddocker-for-desktop&resourceVersion=0: dial tcp 192.168.65.3:6443: getsockopt: connection refused
E0131 10:04:35.404825    1193 reflector.go:205] k8s.io/kubernetes/pkg/kubelet/kubelet.go:413: Failed to list *v1.Service: Get https://192.168.65.3:6443/api/v1/services?resourceVersion=0: dial tcp 192.168.65.3:6443: getsockopt: connection refused
E0131 10:04:36.405465    1193 reflector.go:205] k8s.io/kubernetes/pkg/kubelet/config/apiserver.go:47: Failed to list *v1.Pod: Get https://192.168.65.3:6443/api/v1/pods?fieldSelector=spec.nodeName%3Ddocker-for-desktop&resourceVersion=0: dial tcp 192.168.65.3:6443: getsockopt: connection refused
E0131 10:04:36.405721    1193 reflector.go:205] k8s.io/kubernetes/pkg/kubelet/kubelet.go:422: Failed to list *v1.Node: Get https://192.168.65.3:6443/api/v1/nodes?fieldSelector=metadata.name%3Ddocker-for-desktop&resourceVersion=0: dial tcp 192.168.65.3:6443: getsockopt: connection refused
...
```

This is not a problem: this is `kubelet` trying to connect to API server when
the latter is reading ready yet.
