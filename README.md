# de_microservices_stuff
## Questions
* How is a custom image repository used?
  * https://skaffold.dev/docs/environment/image-registries/ 
## Notes 
* port forward is how endpoints are exposed.
## Technologies
https://www.youtube.com/watch?v=jnxj4Ma3zpg
## Tools
* [Google Cloud SDK/Plugin](https://cloud.google.com/code/docs/intellij/install)

  This plugin can be configured to use and installed skaffold executable or use its own bundled tool.

* [Skaffold - Google developed tool for managing K8s](https://skaffold.dev/)
* [K9s Terminal UI to inspect Kubernetes](https://k9scli.io/topics/install/)
* [minikube local kubernetes](https://minikube.sigs.k8s.io/docs/start/)
* [Docker Desktop](https://www.docker.com/products/docker-desktop/)
  
  Currently I'm using the minikube install rather than the Docker Desktop Kubernetes.

## Resources
*[Youtube video for Skaffold and Kubernetes](https://www.youtube.com/watch?v=Fu5CpVaiE_E)
  * [Gotcha on windows!!!](https://youtu.be/Fu5CpVaiE_E?t=1707)
  * [Helm](https://youtu.be/Fu5CpVaiE_E?t=1780)

# Skaffold Notes
## Features

Allows continuous iteration locally when developing Kubernetes applications.

Pods must be marked as syncable for code changes to be tracked.

**Profiles** allow tools to be swapped out

#### Build
Custom scrpts can also be used for building.

Log aggregation is handled by skaffold.

## [Quick Start](https://skaffold.dev/docs/quickstart/)

Development mode to watch code and redeploy
```scaffold dev```

Run mode deploys code one time
```skaffold run```

**Docker has to be running for the kubernetes cluster to start!!!**

**Kubernetes is disabled in Docker Desktop**

## [Getting Started With Your Project](https://skaffold.dev/docs/workflows/getting-started-with-your-project/)
**NOT DONE*
## [Configuration](https://skaffold.dev/docs/design/config/)
* configurations can be imported using "require"
* Paths are relative to the directory containing the imported configuration file
  * [Configuration Dependencies Tutorial](https://skaffold.dev/docs/tutorials/config-dependencies/) 

## [Skaffold Pipeline](https://skaffold.dev/docs/pipeline-stages/)
**NOT DONE**
## [Architecture and Design](https://skaffold.dev/docs/design/)
**NOT DONE**

# Kubernetes Notes
[Kubernetes in 5 minutes](https://www.youtube.com/watch?v=PH-2FfFD2PU)
pod is th smallest unit of deployment in k8s

The yaml file is fed to the k8s cluster services which builds the workers

# Future Reads
* [Goodbye Docker Desktop, Hello Minikube!](https://itnext.io/goodbye-docker-desktop-hello-minikube-3649f2a1c469)


# Handy Stuff
Kill docker desktop from Powershell:
```
$isrunning = Get-Process "Docker Desktop" -ErrorAction SilentlyContinue
if ($isrunning) {
$isrunning.CloseMainWindow()
$isrunning | Stop-Process -Force
}
```