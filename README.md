# OpenJML Docker
This repo allows you to install easily OpenJML on your machine.

## OpenJML

The Java Modeling Language is a mature program specification language.
OpenJML is capable of checking Java programs annotated with specifications in the Java Modeling Language and provides robust support for many of JML's features.
The goal of the OpenJML project is to implement a full tool for JML and current Java that is easy for practioners and students to use to specify and verify Java programs. In addition, the project seeks to advance the theory and experience of software verification in practical, industrially-relevant contexts.
For more information about it, see the [OpenJML website](https://www.openjml.org/).

## Installation

This repo provide to you two installation mode
### first way
The first one is more fast than the second one, it consist to download the image directly from the dockerhub repo, this modality is more faster because the image is already built.

<br>

```sh
git clone https://github.com/andreabac3/openjml-docker.git
cd openjml-docker
docker-compose up -d

```
### second way
<br>

The second way allow you to use the original Dockerfile and build it.
The original Dockerfile is provided by the original [OpenJML repo](https://github.com/OpenJML/tryopenjml/blob/master/tools/Dockerfile) <br>
```sh
git clone https://github.com/andreabac3/openjml-docker.git
cd openjml-docker/original_dockerfile/
docker-compose up -d

```
<br>

## Shared folder

The docker-compose.yml uses the folder present in the repository as a shared folder between the file system the host and the docker. <br>
The folder is called my_java_code located in the root folder, you can edit your code with your favourite editor/IDE and then execute it into the docker. <br>
HostFS:  openjml-docker/my_java_code/ <br>
DockerFS: /my_java_code <br>

## Execution

```sh
docker exec -it openjml_container java -jar /tools/openjml/openjml.jar my_java_code/file.java
```

# Authors

* **Andrea Bacciu**  [Github profile](https://github.com/andreabac3)