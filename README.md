# Maven-Project-Docker-Project-Structure
Jenkinsfile Using Shared Libraries

How This Works (Conceptual Summary)
1. Jenkinsfile calls @Library('my-shared-lib')

This loads shared functions from your external Git repo.

2. mavenBuild()

Runs mvn clean install -DskipTests.

3. dockerBuild("my-maven-app:latest")

Builds Docker image using the Dockerfile.

4. Jenkins executes all steps in a clean pipeline.
