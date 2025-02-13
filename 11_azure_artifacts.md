# Lesson: Azure Artifacts – Streamlining Artifact Management in CI/CD Pipelines

## Overview

In modern software development, shared code and pre-built packages are crucial for accelerating development and maintaining consistency. These reusable components, often called artifacts, are securely stored and managed in artifact repositories. Azure Artifacts, a key component of Azure DevOps, provides a centralized and secure environment for storing, managing, and sharing software packages. This lesson explores the concepts of artifact repositories, Azure Artifacts, feeds, and artifact management within Azure Pipelines.



## Learning Objectives

By the end of this lesson, you will be able to:
1. Understand the purpose and types of artifact repositories.
2. Explain Azure Artifacts and its supported package types.
3. Differentiate between project-scoped and organization-scoped feeds in Azure Artifacts.
4. Publish and download artifacts in Azure Pipelines using YAML configurations.
5. Utilize Azure Artifacts to streamline CI/CD pipelines effectively.



## Artifact Repositories Overview

Artifact repositories serve as centralized storage for deployable software components. These repositories play a critical role in enabling code reuse, version control, and secure sharing. Artifacts typically fall into two categories:

1. **Build Artifacts:** Generated during the build process, these artifacts are transient and exist only within the pipeline. They include binaries and outputs that facilitate testing and validation.
2. **Deployment Artifacts:** These are versioned, secured executables ready for public or organizational consumption. Deployment artifacts are essential for releasing stable and reliable software.

### Benefits of Artifact Repositories
- **Version Control:** Manage different versions of software packages.
- **Dependency Management:** Simplify dependency handling during builds.
- **Collaboration:** Enable teams to share and reuse code securely.
- **Scalability:** Handle large volumes of artifacts efficiently.



## Introduction to Azure Artifacts

Azure Artifacts is a cloud-based artifact repository integrated into Azure DevOps. It allows developers to store, manage, and share packages and build outputs securely and efficiently. 

### Key Features of Azure Artifacts
- **Wide Package Support:** Supports NuGet, npm, Python, Maven, and universal packages.
- **Build Artifacts Management:** Stores binaries and symbols generated during the build process.
- **Flexible Sharing Options:** Share packages:
  - Internally with team members.
  - Within the organization across projects.
  - Publicly for external use.



## Azure Artifacts Feeds

Azure Artifacts uses feeds to organize and manage software packages. A feed serves as a container for multiple types of packages and provides visibility and accessibility based on scope.

### Project-Scoped Feeds
- **Visibility:** Tied to a specific project, visible to all users with project access.
- **URL Example:**
  ```
  https://pkgs.dev.azure.com/<ORGANIZATION_NAME>/<PROJECT_NAME>/_packaging/<FEED_NAME>/nuget/v3/index.json
  ```
- **Accessibility:** Accessed through the associated project.

### Organization-Scoped Feeds
- **Visibility:** Available across the organization, private by default.
- **URL Example:**
  ```
  https://pkgs.dev.azure.com/<ORGANIZATION_NAME>/_packaging/<FEED_NAME>/nuget/v3/index.json
  ```
- **Accessibility:** Managed from the main feeds menu in Azure Artifacts.



## Managing Artifacts in Azure Pipelines

### Publishing Artifacts in Azure Pipelines

Artifacts generated during a pipeline’s build stage can be published for later use in subsequent stages.

#### Using the Publish Keyword in YAML
The `publish` keyword specifies the path and name of the artifact to be published.
```yaml
steps:
- publish: $(System.DefaultWorkingDirectory)/website/dist
  artifact: website
```
- **`publish`:** Path to the artifact directory.
- **`artifact`:** Unique identifier for the artifact.

#### Using the PublishPipelineArtifact Task
This task provides additional customization options for publishing artifacts.
```yaml
steps:
- task: PublishPipelineArtifact@1
  inputs:
    targetPath: $(System.DefaultWorkingDirectory)/website/dist
    artifactName: website
```
- **`targetPath`:** Path to the folder or file.
- **`artifactName`:** Name of the artifact.



### Downloading Artifacts in Azure Pipelines

Artifacts published in earlier stages can be downloaded in subsequent stages for further processing or deployment.

#### Using the Download Keyword in YAML
The `download` keyword retrieves specific artifacts.
```yaml
steps:
- download: current
  artifact: website
```
- **`download`:** Specifies the artifact source (current pipeline).
- **`artifact`:** Name of the artifact to download.

#### Using the DownloadPipelineArtifact Task
This task provides more flexibility when retrieving artifacts.
```yaml
steps:
- task: DownloadPipelineArtifact@2
  inputs:
    artifact: website
```
- **`artifact`:** Specifies the artifact to download. If omitted, all artifacts are downloaded.



## Best Practices for Azure Artifacts
1. **Organize Feeds:** Use project- and organization-scoped feeds to align with team structures and visibility requirements.
2. **Version Control:** Leverage semantic versioning to manage artifact versions effectively.
3. **Secure Access:** Implement access controls to ensure artifacts are securely shared.
4. **Optimize Pipeline Usage:** Publish and download only necessary artifacts to reduce pipeline overhead.



## Suggested Reading
1. [Azure Artifacts Documentation](https://learn.microsoft.com/en-us/azure/devops/artifacts/)
2. [Managing Feeds in Azure Artifacts](https://learn.microsoft.com/en-us/azure/devops/artifacts/feeds/)
3. [YAML Schema for Azure Pipelines](https://learn.microsoft.com/en-us/azure/devops/pipelines/yaml-schema/)
4. [Best Practices for Artifact Management](https://learn.microsoft.com/en-us/azure/devops/artifacts/concepts/)

