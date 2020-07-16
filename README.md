# Tanzu DevOps/CD Demo

This is the DevOps/CD demo with Tanzu technologies that is shown in this video: 
[![](http://img.youtube.com/vi/jRBGQ3Jhrgw/0.jpg)](http://www.youtube.com/watch?v=jRBGQ3Jhrgw "CI/CD and DevOps with Tanzu")

# Prerequisites

You will want at least one running Kubernetes cluster to install and run the demo. These assets have been tested with TKG Standalone (TKG) and TKG Integrated (TKGI).

This document will refer to a **Shared Services Cluster**, which will control the build and deployment pipelines, and a **Workload Cluster**, which will run the user applications that we build and deploy. The Shared Services Cluster and the Workload cluster could be a single cluster if you are tight on demo resources, but in practice a single Shared Services cluster would service many external Workload Clusters.
