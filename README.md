# mvn-openjdk-8-alpine

## Usage

Please notice this image is configured with a workdir /code, so make sure you mount such volume first.

### General usage

```
$ docker run -v $(pwd):/code ivan97/mvn-openjdk-8-alpine:latest 'your-commands-here'
```

### You can run mvn commands like mvn -v simply:

```
$ docker run -ti --rm ivan97/mvn-openjdk-8-alpine:latest mvn -v
```

### This image can be configured for holding the Maven cache artifacts:

```
$ docker run -ti --rm -v $(pwd):/code -v "$HOME/.m2":/root/.m2 iflavoursbv/mvn-sbt-openjdk-8-alpine:latest mvn clean compile
```

## Configuration

```
This docker image is based on the following stack: - OS: Alpine Linux - Java: OpenJDK 8 - Maven: latest=3.5.2 (see tag list for more versions)
```

## Dependencies

- [java:openjdk-8-jdk-alpine](https://hub.docker.com/r/library/java/tags/openjdk-8-jdk-alpine/)
