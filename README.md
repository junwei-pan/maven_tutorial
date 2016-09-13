# This is a tutorial about maven

## Build & Run

### Generate a Project

```shell
mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

### Build the Package

```shell
mvn package
```

### Run the Code

```shell
java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App
```

## Basic Concepts

### Maven Phases

Although hardly a comprehensive list, these are the most common default lifecycle phases executed.

- **validate**: validate the project is correct and all necessary information is available
- **compile**: compile the source code of the project
- **test**: test the compiled source code using a suitable unit testing framework. These tests should not require the code be packaged or deployed
- **package**: take the compiled code and package it in its distributable format, such as a JAR.
- **integration-test**: process and deploy the package if necessary into an environment where integration tests can be run
- **verify**: run any checks to verify the package is valid and meets quality criteria
- **install**: install the package into the local repository, for use as a dependency in other projects locally
- **deploy**: done in an integration or release environment, copies the final package to the remote repository for sharing with other developers and projects.

There are two other Maven lifecycles of note beyond the default list above. They are

- **clean**: cleans up artifacts created by prior builds
- **site**: generates site documentation for this project

## References

1. [Maben in 5 Minutes](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)
2. [Introduction to the Build Lifecycle](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)

# maven_tutorial
