# Devcontainer Dockerfile

# Use the official image as a parent image
FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu-20.04

# Install PowerShell
RUN apt-get update && \
    apt-get install -y wget apt-transport-https software-properties-common && \
    wget -q https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb && \
    dpkg -i packages-microsoft-prod.deb && \
    apt-get update && \
    apt-get install -y powershell

# Install .NET SDK
RUN wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb && \
    dpkg -i packages-microsoft-prod.deb && \
    apt-get update && \
    apt-get install -y dotnet-sdk-5.0

# Install Node.js
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash - && \
    apt-get install -y nodejs

# Install additional libraries or packages required by the project
# (Add any additional installation commands here)

# Set the default shell to bash
SHELL ["/bin/bash", "-c"]
