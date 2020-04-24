# compliance-evidence-locker

This is a template repository to clone compliance-evidence-locker for reference compliance toolchain templates.

## Purpose of this repository

This repository serves as the evidence locker for tasks in the reference compliance toolchain.

### Folder structure

Evidence output is structured in a simple folder structure:

```
/raw
├── ci
│   ├── _PIPELINE_RUN_ID_A1
│   ├── _PIPELINE_RUN_ID_A2
│   ├── .. 
│   └── _PIPELINE_RUN_ID_An
└── cd
    ├── _PIPELINE_RUN_ID_B1
    ├── _PIPELINE_RUN_ID_B2
    ├── .. 
    └── _PIPELINE_RUN_ID_Bn
```

Evidence collected from CI and CR pipelines stored under a folder that is named after the pipeline run id. Therefore it's easy to identify and link to the original pipeline run within a toolchain and pipeline.

_**Note:** this is still work in progress_

### File structure

Collected evidence inside each folder named of the Pipeline run is separated within files. File naming should reflect the pipeline task that provided that evidence.

### Evidence Summary

At the end of the CD run, all collected evidence from CD and CI runs that are related to the deployment will be summarized in a JSON file. This summary refers to the other summary files in detail and can be parsed later for a compliance audit.

## Further references

* [Evidence summary structure plans](https://github.ibm.com/cocoa/board/issues/227)
* [Devops section of the IBM Cloud Engineering handbook](https://pages.github.ibm.com/CloudEngineering/system_architecture/devops/)
* [Reference compliance CI toolchain](https://github.ibm.com/one-pipeline/compliance-ci-toolchain)
* [Reference compliance CD toolchain](https://github.ibm.com/one-pipeline/compliance-cd-toolchain)
* [Compliance related commont Tekton tasks](https://github.ibm.com/one-pipeline/common-tekton-tasks)
* [Tekton CD/CI Pipelines](https://github.com/tektoncd/pipeline)
