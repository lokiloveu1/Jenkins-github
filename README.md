# Jenkins-github

This pipeline defines a Jenkins pipeline with four stages: “Clone Repository”, “Build”, “Test”, and “Deploy”.

The “Clone Repository” stage checks out the code from a GitHub repository using the repository URL and branch name from the environment variables.
The “Build” stage runs a command to build the application using Gradle.
The “Test” stage runs a command to test the application using Gradle.
The “Deploy” stage runs a command to deploy the application using a shell script.
The post-build action sends the build status to GitHub with a context of “continuous-integration/jenkins” and state of “success”, and also adds a comment on Github like “The pipeline completed successfully!” and adds a label ‘approved’.
