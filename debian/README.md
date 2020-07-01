# SBT

With this docker image, you can run sbt without having it installed.

## Build

There are two images to build:

* One with just sbt
* One with sbt and sonarscanner

```bash
docker build -t bunyodb/sbt:<java-version>_<sbt-version> -f Dockerfile_<java-version>_<sbt-version> .
```

Obviously, replacing the placeholders with the right versions. Example:

For java 8, sbt 1.2.8
```bash
docker build -t bunyodb/sbt:8u212_1.2.8 -f Dockerfile_8u212_1.2.8 .
```

For java 11, sbt 1.3.12, sonar scanner 3.3.0
```bash
docker build -t bunyodb/sbt:11.0.5_1.3.12 -f Dockerfile_11.0.5_1.3.12 .
```


```bash
docker run bunyodb/sbt:11.0.5_1.3.12
```