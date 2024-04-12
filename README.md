# Tekton Demo

This repository contains demo which is done to show the use case of CustomRuns in Tekton.

### Prerequisite setup

You will need a k8s cluster with [Tekton Pipelines](https://github.com/tektoncd/pipeline/blob/main/docs/install.md) installed in it.

### Tekton

This is just simple vanilla tekton example.

Steps

* Create task from `tekton/task.yaml`
* Create pipeline from `tekton/pipeline.yaml`
* Create workspace from `tekton/workspace.yaml`
* Create pipelinerun from `tekton/pipelinerun.yaml`

### Tekton With Custom Controller

This is same example as above but contains an extra task which demonstrates the use case of
CustomRun and Custom Controller. This will show how we can perform an operation without creating
kubernetes resources.

Steps

* Install the custom controller from [here](https://github.com/tektoncd/pipeline/tree/main/test/custom-task-ctrls/wait-task-beta) using

	```
	ko apply -f config/ from
	```
* You can use the task and workspace which we installed in the above vanilla Tekton example
* Create pipeline from `tekton-with-custom-controller/pipeline.yaml`
* Create pipelinerun from `tekton-with-custom-controller/pipelinerun.yaml`


### Tekton With Custom Task and Controller

This is same example as above but contains an extra task which demonstrates the use case of
CustomTask, CustomRun and Custom Controller. This will show how a pipeline can keep waiting
for human intervention and proceed further based on input.

Steps


* Install the CustomTask and controller from [here](https://github.com/openshift-pipelines/manual-approval-gate/tree/main/config) using

	```
	ko apply -f config/kubernetes
	```
* You can use the task and workspace which we installed in the above vanilla Tekton example
* Create pipeline from `tekton-with-custom-task-and-controller/pipeline.yaml`
* Create pipelinerun from `tekton-with-custom-task-and-controller/pipelinerun.yaml`

