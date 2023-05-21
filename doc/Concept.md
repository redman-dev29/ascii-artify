# ascii-artify
Description and characteristics of tools for local development of the ASCII-Artify project.

>This repository is created to compare different application launch and testing tools against the original repository:
>https://github.com/Gopal9816/ASCII-Artify
---
#### 1. Three tools were chosen for testing:
* [minikube](https://minikube.sigs.k8s.io/docs/) - is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes. All you need is Docker (or similarly compatible) container or a Virtual Machine environment, and Kubernetes is a single command away: `minikube start`
* [kind (k8s in Docker)](https://kind.sigs.k8s.io/) - is a tool for running local Kubernetes clusters using Docker container “nodes”. kind was primarily designed for testing Kubernetes itself, but may be used for local development or CI. If you have go 1.16+ and docker or podman installed ```go install sigs.k8s.io/kind@v0.19.0 && kind create cluster is all you need!```
* [k3d](https://k3d.io/) - is a lightweight wrapper to run k3s (Rancher Lab’s minimal Kubernetes distribution) in docker. k3d makes it very easy to create single- and multi-node k3s clusters in docker, e.g. for local development on Kubernetes.


|                      |       minikube                    |       kind           |       k3d            |
|:---------------------|:---------------------------------:|:--------------------:|:--------------------:|
|Support OS:           | Linux, macOS, Windows             | Linux, macOS, Windows| Linux, macOS, Windows|
|Architectures:        | x86-64, arm64, armv7, ppc64, s390x| x86-64, arm64        | x86-64, arm64, armv7 |
|Additional functions: | Addons                            |                      |                      |
|Monitoring:           | Integrated K8S Dashboard UI       |                      |                      |
|Container Manager[^1]:| Docker, Podman                    | Docker, Podman       | Docker, Podman       |
|Managing Kubernetes:  | Kubectl                           | Kubectl              |                      |  

[^1]: To avoid [Docker licensing](https://www.docker.com/pricing/) issues, [Podman](https://docs.podman.io/en/latest/) can be used as an alternative. But remember, Podman is an experimental driver. Please use it only for experimental reasons until it has reached maturity. For a more reliable minikube experience, use a Docker.
_ _ _
#### 2. After testing these three tools, we have the following results:

|                            |       minikube             |       kind               |       k3d            |
|:---------------------------|:--------------------------:|:------------------------:|:--------------------:|
|Ease of use:                | :heavy_check_mark:         | :x:                      | :x:                  |
|Deployment speed:           | :heavy_check_mark:         | :x:                      | :x:                  |
|Stability of work:          | :heavy_check_mark:         | :x:                      | :heavy_check_mark:   |
|Complexity of setup and use:| :heavy_check_mark:         | :x:                      | :x:                  |
|Documentation:              | :heavy_check_mark:         | :heavy_check_mark:       | :heavy_check_mark:   |
|Community support:          | Slack, Twitter, GitHub     | Slack, GitHub, Email list| Slack                |
_ _ _
#### 3. The final step is to deploy the "Hello World" application to the Kubernetes cluster.
* Deploying a "Hello world" application to a Kubernetes cluster using **minikube**.
![Image](.data/minikube_demo.gif)


