# Kubernetes Manifests for Node.js App 
## Overview
This repo contains Kustomize-based Kubernetes manifests for dev and prod environments.

![CICD diagram](https://github.com/user-attachments/assets/5d81856f-c8d7-4273-b4cd-5f0cda914c21)


## Features

- Separate overlays for dev and prod.

- Integration with Argo CD for GitOps deployment.

- Automated updates to image tags from the app repo.

## Project Structure


```
base/
  deployment.yaml
  service.yaml
overlays/
  dev/kustomization.yaml
  prod/kustomization.yaml
```
## How it works

Argo CD watches this repo and syncs changes automatically.

When image tags are updated by the CI pipeline, Argo CD deploys new versions.

### Links

https://github.com/tobi-willy/CICD-pipeline-project

