# swift-vscode-remote-container-docker

The Docker image created with this Dockerfile is intended to be used
with Visual Studio Code via the [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension for projects written in [Swift](https://swift.org/documentation/#the-swift-programming-language).

This Dockerfile is also published to Docker Hub as [paulbuis/swift-vscode-remote-container-docker](hub.docker.com/r/paulbuis/swift-vscode-remote-docker/)

The devcontainer.json and Dockerfile belong in the .devcontainer directory of your project as described in [Ian nPartridge's Medium article](https://medium.com/@ianpartridge/swift-development-in-docker-using-visual-studio-code-remote-b84d035e70db). See his [GitHub example](https://github.com/ianpartridge/vscode-remote-try-swift) for the needed .vscode directory as well.

To run the container and get a bash prompt from which you can run the swift interpreter, use the command:
``` bash
docker run -it -u vscode --cap-add=SYS_PTRACE --security-opt seccomp=unconfined swift-vscode-remote-container-docker bash
```