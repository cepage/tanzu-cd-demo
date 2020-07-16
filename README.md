# Tanzu DevOps/CD Demo

This is the DevOps/CD demo with Tanzu technologies that is shown in this video: 
[![](http://img.youtube.com/vi/jRBGQ3Jhrgw/0.jpg)](http://www.youtube.com/watch?v=jRBGQ3Jhrgw "CI/CD and DevOps with Tanzu")

# Prerequisites

You will want at least one running Kubernetes cluster to install and run the demo. These assets have been tested with TKG Standalone (TKG) and TKG Integrated (TKGI).

This document will refer to a **Shared Services Cluster**, which will control the build and deployment pipelines, and a **Workload Cluster**, which will run the user applications that we build and deploy. The Shared Services Cluster and the Workload cluster could be a single cluster if you are tight on demo resources, but in practice a single Shared Services cluster would service many external Workload Clusters.

# Installation

First, install ArgoCD onto the Shared Services cluster. It's a simple install, and the instructions are here: https://argoproj.github.io/argo-cd/getting_started/. If your workload cluster is separate from the Shared Services cluster, you must register the workload cluster as described here: https://argoproj.github.io/argo-cd/getting_started/

Second, install Tanzu Build Service onto the Shared Services cluster. This is the most complicated installation piece, and documentation is here: https://docs.pivotal.io/build-service/0-2-0/index.html. This installation process includes configuring the Docker repository that build service will be publishing images to (and that our deployment engine will be pulling from).

