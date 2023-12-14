# Benchmarking Kubernetes distributions for use in a local development environment.

The next two tables contain general and feature comparisons of Kubernetes distributions that we are considering for integration into the local developer workspace.

| **Aspect**                   | **Minikube**                                                               | **k3d (K3s in Docker)**                                     | **kind (Kubernetes in Docker)**                             |
|------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------|------------------------------------------------------------|
| **Ease of Use**               | Designed for easy setup and use for local development and testing.        | Lightweight and easy to use, suitable for rapid development. | Fast and customizable, ideal for local development and testing. |
| **Cross-Platform**            | Works on Windows, macOS, and Linux.                                      | Compatible across different platforms.                        | Platform-agnostic, works on various operating systems.      |
| **Resource Footprint**        | Can be resource-intensive, especially on machines with limited resources. | Designed to be lightweight, with a smaller footprint.         | Known for its speed and lightweight nature.                 |
| **Startup Speed**             | May have slower startup times compared to lighter alternatives.          | Tends to start up quickly, efficient for rapid development.   | Fast startup, suitable for rapid local development.         |
| **Docker Integration**        | Utilizes a virtual machine for running Kubernetes.                        | Integrates with Docker, leveraging container orchestration.  | Leverages Docker for creating and managing Kubernetes nodes. |
| **Customization**             | Supports various add-ons for additional features.                        | Limited production use, primarily for local development.     | Customizable and extensible, providing flexibility.         |
| **Community Support**         | Well-established community with ample documentation.                      | Smaller community compared to Minikube.                      | Smaller community compared to more established tools.      |
| **Production Suitability**    | Primarily used for local development and testing.                        | Limited production use, better suited for development.        | Not designed for production but can be used for testing.    |

| **Feature**                   | **Minikube**                                                               | **k3d (K3s in Docker)**                                     | **kind (Kubernetes in Docker)**                             |
|------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------|------------------------------------------------------------|
| **Container Runtime**               | containerd cri-o docker        | containerd docker  | docker cri-o |
| **Multinode cluster**            | + (require CSI Hostpath Driver addon)                                      | +                 |+    |
| **Multiserver cluster**        | - | +        | +               |
| **LoadBalancer**             | +          | +  | + (needs additional installation steps)     |
| **Local Container Registry**        | +                        | +  | + |
| **Non-default CNI**             | Calico | Calico   | Calico        |
| **declarative cluster configuration**         | -                      | + (yaml in an Alpha State)                     | +    |
| **Podman**    | + (experemental)                        | +     | +   |

The basic setup steps for each of the three Kubernetes distributions are shown in the next short demos.

## Minikube

![minikube](https://github.com/bergshrund/AsciiArtify/assets/17909431/0bcb7be0-41df-4800-a958-13d85b9e0e72)

## Kind

![kind](https://github.com/bergshrund/AsciiArtify/assets/17909431/ea3e4a67-6dff-49de-b74c-a08be304e0d6)

## k3d

![k3d](https://github.com/bergshrund/AsciiArtify/assets/17909431/a43fd9bf-c6e7-4d49-aa29-2f354e0e6096)

## Summary

- **Minikube:** Good for beginners and those who prioritize ease of use. Suitable for local development and testing, but it can be resource-intensive.
- **k3d:** Lightweight and fast, making it a good choice for local development. However, it might not be the best fit for production environments.
- **kind:** Fast and customizable, ideal for local development and testing. While it lacks some features for production, it's well-suited for rapid development cycles.
