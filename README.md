# Bridge for SLF4J API of Apache RocketMQ

[![License][license-image]][license-url]
[![build][build-image]][build-url]
[![Maven Central][maven-image]][maven-url]

## Introduction

This project bridges the SLF4j API revealed in [rocketmq-logging](https://github.com/aliyunmq/rocketmq-logging) to
standard [SLF4J API](https://github.com/qos-ch/slf4j).

Basically, the project hijacks the implementation of standard SLF4J and delegates it to implement
the [SLF4J API of Apache RocketMQ](https://github.com/aliyunmq/rocketmq-logging/tree/master/rocketmq-slf4j-api).

## Requirements

- Java 1.8 or later

## Getting Started

Add the following dependency to your project. Remember to:

* Replace `ROCKETMQ-LOGGING-VERSION` with
  the [latest release](https://search.maven.org/search?q=g:io.github.aliyunmq%20AND%20a:rocketmq-logging).
* Replace `ROCKETMQ-SLF4J-API-BRIDGE-VERSION` with
  the [latest release](https://search.maven.org/search?q=g:io.github.aliyunmq%20AND%20a:rocketmq-slf4j-api-bridge).

```xml
<dependencies>
    <dependency>
        <groupId>io.github.aliyunmq</groupId>
        <artifactId>rocketmq-slf4j-api</artifactId>
        <version>ROCKETMQ-LOGGING-VERSION</version>
    </dependency>
    <dependency>
        <groupId>io.github.aliyunmq</groupId>
        <artifactId>rocketmq-slf4j-api-bridge</artifactId>
        <version>ROCKETMQ-SLF4J-API-BRIDGE-VERSION</version>
    </dependency>
</dependencies>
```

## Manual Release

Set the password in your `settings.xml` for repositories: `sonatype-nexus-snapshots-aliyunmq`
and `sonatype-nexus-staging-aliyunmq`, then execute the command below:

```bash
mvn clean deploy -Prelease
```

Sign in [nexus repository manager](https://s01.oss.sonatype.org/#stagingRepositories) and check the artifact, then determine whether to release it.

## Related Projects

* [rocketmq-logging](https://github.com/aliyunmq/rocketmq-logging): Logging for Apache RocketMQ.

## License

[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html) Copyright (C) Apache Software Foundation

[license-image]: https://img.shields.io/badge/license-Apache%202-4EB1BA.svg
[license-url]: https://www.apache.org/licenses/LICENSE-2.0.html
[build-image]: https://github.com/aliyunmq/rocketmq-slf4j-api-bridge/actions/workflows/build.yml/badge.svg
[build-url]: https://github.com/aliyunmq/rocketmq-slf4j-api-bridge/actions/workflows/build.yml
[maven-image]: https://maven-badges.herokuapp.com/maven-central/io.github.aliyunmq/rocketmq-slf4j-api-bridge/badge.svg
[maven-url]: https://maven-badges.herokuapp.com/maven-central/io.github.aliyunmq/rocketmq-slf4j-api-bridge
