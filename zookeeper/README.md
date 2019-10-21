# H07 - Getting Started with Apache Kafka

Denise Case

Northwest Missouri State University

44-517 Big Data

## Prerequisites

You must have recent JDK installed. Recommendation - install Chocolatey, the Windows Package Manager. Then open PowerShell here as Administrator and run:

```PowerShell
choco install openjdk11 -y
```

## Overview

Short introduction to the Kafka distributed streaming platform

We will:

1. Start ZooKeeper (clientPort=2181)
2. Start Kafka (connects to Zookeeper)
3. Create a topic ("bearcat_messages")
4. List topics (to verify)
5. Run a producer. Send messages on our topic.
6. Run a consumer. Get messages on our topic.

## Getting Started

- Fork this repo to your Bitbucket.
- Clone your Bitbucket repo down to your local computer.

## Working in Windows vs Bash

This repo is set with helper batch files that work in Windows. Windows uses a backslash in file paths and accesses .bat Windows Command Line batch files found in the kafka bin/windows folder.

Bash uses a forward slash and must access the .sh shell scripts found in the kafka bin folder.

For Bash script examples, try: <https://bitbucket.org/turingloop/h07>

## Understand the Contents

These helper files are for convenience only - modify them and make them your own. You must understand the contents of the files and how they work.

## Start ZooKeeper on port 2181

In Windows File Explorer:

- Navigate to your h07 folder.
- Right-click on your repo folder and "Open Command Window Here as Administrator".
- Run the batch file to start the Zookeeper service. Keep this window open to keep the service running.

```dos
01start_zookeeper
```

## Start Kafka

Open another Command Window as Admin and start Kafka. Keep this window open to keep Kafka running.

```dos
02start_kafka
```

Kafka will start and connect to ZooKeeper

## Create topic (bearcat_messages)

Open another Command Window as Admin and create a topic.

```dos
03create_topic
```

This will create a new topic named bearcat_messages.

List topics to see all topics (including your new bearcat_messages).

```dos
04list_topics
```

## Create producer (on port 9092)

Open another Command Window as Admin and run a message producer.

```dos
11run_producer
```

While the producer is running, add some messages on the topic.

```dos
  Message 1 - Go Bearcats!
  Message 2 - Forever green!!
```

## Create consumer (listening on port 9092)

Open another Command Window as Admin and run a message consumer.

```dos
21run_consumer
```

Arrange your producer and consumer command windows beside each other to watch the results.

## Troubleshooting

- Path error: The Windows path cannot be too long. If you get a path length error, please clone the repo to your C:\Users\yourusername folder.
- Java error: If you get a Java, JDK, JRE, or JVM error, install the most current version of the JDK as noted in prerequisites.
- wmic error: wmic stands for Windows Management Instrumentation Command-line. Try installing the most current version of TortoiseGit (to get an updated Cygwin) and be sure your environment variables are set.

## Resources and References

Apache Kafka <https://kafka.apache.org/>

How to add "Open Command Window Here as Administrator" to context menu:
<https://www.sevenforums.com/tutorials/47415-open-command-window-here-administrator.html>

Verify Mrakdown with <http://dillinger.io/>
