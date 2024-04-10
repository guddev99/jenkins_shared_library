# Jenkins Shared Library

This repository contains a Jenkins Shared Library that provides reusable Groovy scripts for various CI/CD tasks. These scripts are designed to streamline the development and deployment processes within a Jenkins pipeline.

## Scripts Overview

### QualityGateStatus.groovy
- **Purpose:** Allows waiting for a Quality Gate status without aborting the pipeline.
- **Usage:** `QualityGateStatus(credentialsId)`

### dockerBuild.groovy
- **Purpose:** Builds a Docker image based on provided project, image tag, and Docker Hub username.
- **Usage:** `dockerBuild(project, ImageTag, hubUser)`

### dockerImageCleanup.groovy
- **Purpose:** Cleans up a Docker image based on provided project, image tag, and Docker Hub username.
- **Usage:** `dockerImageCleanup(project, ImageTag, hubUser)`

### dockerImagePush.groovy
- **Purpose:** Pushes a Docker image to a Docker registry (e.g., Docker Hub) after logging in with provided credentials.
- **Usage:** `dockerImagePush(project, ImageTag, hubUser)`

### dockerImageScan.groovy
- **Purpose:** Performs a vulnerability scan on a Docker image using Trivy.
- **Usage:** `dockerImageScan(project, ImageTag, hubUser)`

### gitCheckout.groovy
- **Purpose:** Checks out a specific branch from a Git repository.
- **Usage:** `gitCheckout(stageParams)`

### jarPushJFrog.groovy
- **Purpose:** Pushes a JAR artifact to JFrog Artifactory.
- **Usage:** `jarPushJFrog()`

### mvnBuild.groovy
- **Purpose:** Builds a Maven project while skipping tests.
- **Usage:** `mvnBuild()`

### mvnIntegrationTest.groovy
- **Purpose:** Runs integration tests for a Maven project while skipping unit tests.
- **Usage:** `mvnIntegrationTest()`

### mvnTest.groovy
- **Purpose:** Runs unit tests for a Maven project.
- **Usage:** `mvnTest()`

### statiCodeAnalysis.groovy
- **Purpose:** Performs static code analysis using SonarQube.
- **Usage:** `statiCodeAnalysis(credentialsId)`

You can add this line in the "How to Use" section of your README, right after the instructions for configuring Jenkins to use the shared library. Here's how you can incorporate it:

## How to Use

1. Clone this repository to your Jenkins server or to a location accessible by your Jenkins pipeline.
2. Configure Jenkins to use this repository as a Shared Library.
3. Ensure that the Jenkinsfile in your project references this Shared Library. If you're using the example repository [java-docker-build-pipeline](https://github.com/guddev99/java-docker-build-pipeline), it already utilizes this Shared Library. Otherwise, make necessary adjustments to your Jenkinsfile to incorporate the library's scripts.
4. Utilize the provided scripts in your Jenkins pipelines by calling them with the appropriate parameters.

