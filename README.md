# Tekton Demo

This repository contains demo which is done to show the use case of CustomRuns in Tekton.

### Tekton

This is just simple vanilla tekton example.

### Tekton With Custom Controller

This is same example as above but contains an extra task which demonstrates the use case of
CustomRun and Custom Controller. This will show how we can perform an operation without creating
kubernetes resources.

### Tekton With Custom Task and Controller

This is same example as above but contains an extra task which demonstrates the use case of
CustomTask, CustomRun and Custom Controller. This will show how a pipeline can keep waiting
for human intervention and proceed further based on input.

### Prerequisite setup

1. Create a k8s cluster
2. Install Tekton
3. Install CustomTask and Controller for both the examples