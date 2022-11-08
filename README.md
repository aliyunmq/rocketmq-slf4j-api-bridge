# Bridge for SLF4j API of Apache RocketMQ

[![License][license-image]][license-url]
[![build][build-image]][build-url]

## Introduction

This project bridges the SLF4j API revealed in [rocketmq-logging](https://github.com/aliyun-mq/rocketmq-logging) to standard [SLF4j API](https://github.com/qos-ch/slf4j).

## Requirements

- Java 1.8 or later

## Manual Release

Set the password in your `settings.xml` for repositories: `sonatype-nexus-snapshots-aliyun-mq`
and `sonatype-nexus-staging-aliyun-mq`, then execute the command below:

```bash
mvn clean install -Prelease
```

Sign in [nexus repository manager](https://s01.oss.sonatype.org/#stagingRepositories) and check the artifact, and
determine to release/drop it.

## License

[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html) Copyright (C) Apache Software Foundation

[license-image]: https://img.shields.io/badge/license-Apache%202-4EB1BA.svg
[license-url]: https://www.apache.org/licenses/LICENSE-2.0.html
[build-image]: https://github.com/aliyun-mq/rocketmq-slf4j-api-bridge/actions/workflows/build.yml/badge.svg
[build-url]: https://github.com/aliyun-mq/rocketmq-slf4j-api-bridge/actions/workflows/build.yml