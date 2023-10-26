# Tetris Web Game on Kubernetes with ArgoCD👾

Welcome to the Tetris Web Game project 🕹👨‍💻, which runs the classic Tetris game on Kubernetes using ArgoCD for GitOps-based deployment. In this project, you'll find everything you need to deploy and enjoy the Tetris game in a scalable and automated way.

![Tetris](https://github.com/s1mba10/argocd-tetris/assets/101098236/bb387687-2701-4910-9ef7-1817039a6d72)


## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Deployment](#deployment)
- [Usage](#usage)


## Overview

Tetris is a beloved classic video game where players arrange falling blocks to complete lines and clear the game board. This project brings the Tetris game to the web, making it accessible to a broader audience. With Kubernetes and ArgoCD, you can effortlessly deploy, manage, and update the game, ensuring that you always have the latest version.

## Prerequisites

Before you begin, ensure you have the following prerequisites in place:

- [Kubernetes](https://kubernetes.io/) cluster set up.
- [ArgoCD](https://argoproj.github.io/argo-cd/) installed and configured in your Kubernetes cluster.

## Getting Started

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/s1mba10/argocd-tetris.git
   ```

2. Change to the project directory:

   ```bash
   cd argocd-tetris
   ```

3. Customize the Tetris game configuration as needed by modifying the `config.yaml` file.

## Deployment

To deploy the Tetris game on your Kubernetes cluster using ArgoCD, follow these steps:

1. Login to ArgoCD:

   ```bash
   argocd login <ARGOCD_SERVER>
   ```

2. Create an ArgoCD Application for the Tetris game:

   ```bash
   argocd app create tetris --repo https://github.com/s1mba10/argocd-tetris.git --path manifests --dest-server https://kubernetes.default.svc --dest-namespace default --sync-policy automated
   ```

Once the synchronization is complete, the Tetris game will be available on your Kubernetes cluster.
![ArgoCD ready application](https://github.com/s1mba10/argocd-tetris/assets/101098236/e6c55a42-1340-44e2-9300-70201b1e3cd7)


## Usage

Access the Tetris game by opening a web browser and navigating to the following URL:

```
https://<tetris-service-ip>:80
```
Enjoy playing Tetris, and happy coding! 🎮🚀
