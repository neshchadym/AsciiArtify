# AsciiArtify Kubernetes Deployment Tools Evaluation
## Introduction
Minikube: Minikube is a tool that allows you to run Kubernetes locally. It creates a single-node Kubernetes cluster inside a virtual machine on your laptop for users looking to try out Kubernetes or develop with it day-to-day.

Kind: Kind, short for Kubernetes in Docker, is a tool for running local Kubernetes clusters using Docker container “nodes”. Kind was primarily designed for testing Kubernetes itself, but may be used for local development or CI.

k3d: k3d is a lightweight wrapper to run Rancher Lab’s k3s in Docker. k3s is a highly available, certified Kubernetes distribution designed for production workloads in unattended, resource-constrained, remote locations or inside IoT appliances. With k3d, you can create single-node and multi-node k3s clusters in Docker, for local development on Kubernetes, or as temporary testing environment.

## Characteristics
### Minikube
Runs a local Kubernetes cluster on macOS, Linux, and Windows1.
It supports the latest Kubernetes release and six previous minor versions.
It has advanced features such as LoadBalancer, filesystem mounts, FeatureGates, and network policy.
It also supports addons for easily installed Kubernetes applications.

### Kind
Allows you to run Kubernetes on your local computer.
This tool requires that you have either Docker or Podman installed.
It’s flexible and allows you to customize your cluster by adding or removing nodes, changing configuration settings, and installing additional software.

### k3d
Lightweight wrapper to run Rancher Lab’s k3s in Docker.
It makes it very easy to create single- and multi-node k3s clusters in Docker.
As of k3d version v4.0.0, k3d’s abilities include creating/stop/start/delete/grow/shrink K3s clusters (and individual nodes) via command line flags or via a configuration file.
It can manage and interact with container registries that can be used with the cluster.
It can manage Kubeconfigs for the clusters.
It can import images from your local Docker daemon into the container runtime running in the cluster.

## Advantages and Disadvantages
| **Pros and Cons** | **Minikube** | **Kind** | **k3d** |
|-------------------|--------------|----------|---------|
| **Pros** | + Easy to use<br>+ Suitable for local development and testing<br>+ Supports the latest Kubernetes release and six previous minor versions<br>+ Has advanced features such as LoadBalancer, filesystem mounts, FeatureGates, and network policy<br>+ Supports addons for easily installed Kubernetes applications | + Suitable for local development and testing<br>+ Works within Docker containers<br>+ Flexible and allows customization of the cluster | + Suitable for local development and testing<br>+ Works within Docker containers<br>+ Fast cluster creation and testing<br>+ Can manage and interact with container registries that can be used with the cluster<br>+ Can manage Kubeconfigs for the clusters<br>+ Can import images from your local Docker daemon into the container runtime running in the cluster |
| **Cons** | + Only designed for testing<br>+ New versions can have broken features<br>+ Networking can be unreliable<br>+ Documentation is not always in sync | + Does not have a built-in LoadBalancer, so you'll need to install one manually if you need LoadBalancer services<br>+ Does not support Windows containers | + Most legacy components, optional drivers, and plugins are unavailable in K3S<br>+ Configures everything automatically; doing custom configuration is difficult and requires good system knowledge |


