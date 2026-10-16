# Awesome-AMQP-Client-Libraries

# Top AMQP Client Libraries Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on AMQP Protocol Implementations, Message Brokers & Client Library Abstractions*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **AMQP Client Libraries**. These tools enable developers to implement the Advanced Message Queuing Protocol across languages and frameworks—providing high-level abstractions for publishing, consuming, and routing messages through brokers like RabbitMQ, ActiveMQ, and cloud messaging services.

**Examples** include Kombu, Pika, Celery, RabbitMQ, Amazon SQS, Azure Service Bus, Redis Streams, Google Cloud Pub/Sub, ActiveMQ, and Kafka Python (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, protocol implementation, and open messaging infrastructure—ideal for developers, platform teams, and architects seeking transparent, vendor-independent message queuing.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Amazon SQS](https://aws.amazon.com/sqs/)**  
  Fully managed message queuing service for decoupling distributed systems. Features **standard queues** (at-least-once delivery) and **FIFO queues** (exactly-once processing) . Supports **dead-letter queues**, **visibility timeout**, and **server-side encryption** with AWS KMS . **Scales transparently** to handle any load without provisioning .

- **[Azure Service Bus](https://azure.microsoft.com/en-us/products/service-bus/)**  
  Fully managed enterprise message broker with **queues and publish-subscribe topics** . Features **message sessions** for FIFO guarantees, **auto-forwarding**, **dead-letter queues**, and **durable subscriptions** . Messages persisted in **triple-redundant storage** across availability zones . Pull-based delivery with long-running operations .

- **[Google Cloud Pub/Sub](https://cloud.google.com/pubsub)**  
  Asynchronous messaging service decoupling senders and receivers. Features **pull subscriptions** (unary Pull RPC and StreamingPull), **push subscriptions** with webhook delivery, **BigQuery subscriptions** for direct data warehousing, and **Cloud Storage subscriptions** for cost-effective large-volume storage . Supports **ordering keys** for message ordering .

- **[RabbitMQ Cloud (Tanzu)](https://www.rabbitmq.com/)**  
  Commercial edition of RabbitMQ with enterprise-grade plugins. **RabbitMQ 4.3** adds **JMS queue type** backed by Raft for JMS applications, **JMS message selectors** with SQL-like syntax, **Queue Browser** for non-destructive message inspection, **Message Delivery Delay**, and **Apache Spark Connector** for high-speed data transfer between RabbitMQ Streams and Spark clusters . Supports **AMQP 1.0, 0.9.1, STOMP, and MQTT** .

- **[Redis Cloud](https://redis.io/)**  
  Managed Redis with **Streams** for event messaging. Features **consumer groups**, **automatic retries**, **dead-letter queues**, and **stale message recovery** .

## Open-Source GitHub Projects

- **[Pika](https://github.com/pika/pika)**  
  **The pure-Python implementation of the AMQP 0-9-1 protocol including RabbitMQ's extensions** (BSD-3-Clause) . **The most widely used Python AMQP client library.** Supports Python 3.7+ (CPython and PyPy). **Multiple connection adapters**: `BlockingConnection` (synchronous), `SelectConnection` (asynchronous without dependencies), `AsyncioConnection` (asyncio), `GeventConnection`, `TornadoConnection`, and `TwistedProtocolConnection` . **Thread-agnostic design**—core takes care not to forbid threads, greenlets, callbacks, continuations, or generators . Supports **multiple connection parameters** for fault-tolerance with automatic retries . **Requesting message acknowledgements from another thread** supported via delegation pattern . Used by AWS for **Amazon MQ for RabbitMQ** with TLS configuration .

- **[Kombu](https://github.com/celery/kombu)**  
  **The AMQP Messaging Framework for Python** (BSD-3-Clause) . **Aims to make messaging in Python as easy as possible by providing an idiomatic high-level interface for the AMQP protocol** . **Pluggable transports**—supports multiple message server solutions without changing application code . **Automatic encoding, serialization, and compression** of message payloads . **Graceful handling of connection and channel errors** . **The messaging layer powering Celery** .

- **[Celery](https://github.com/celery/celery)**  
  **Distributed Task Queue** (BSD-3-Clause) . **The standard Python task queue**—communicates via messages using a broker to mediate between clients and workers . **Supports RabbitMQ, Redis, Amazon SQS, and more** as message transports . Features **high availability** (workers and clients retry on connection loss), **fast** (millions of tasks per minute with sub-millisecond latency using RabbitMQ), and **flexible** (custom pools, serializers, compression, schedulers, consumers, producers, autoscalers) . **Framework integration** with Django, Flask, and others .

- **[rabbitmq-client (Node.js)](https://github.com/cody-greene/node-rabbitmq-client)**  
  **Node.js client library for RabbitMQ** (MIT) . **No dependencies** . Features **automatic re-connect, re-subscribe, or retry publishing** . **Higher-level Consumer/Publisher API** for robustness—abstracts away connection loss, channel closure, and consumer cancellation edge-cases . **RPCClient** for request-response communication between services . **Written in TypeScript** with heavily commented type definitions . Performance comparable to amqplib . Requires **RabbitMQ 4.1.x+** for version 5.0.3+ .

- **[AMQPNetLite](https://github.com/azure/amqpnetlite)**  
  **Lightweight AMQP 1.0 library for .NET platforms** (MIT) . Supports **.NET Framework, .NET Micro Framework, .NET Core, Universal Windows Platform, Windows Phone, Windows Store, Mono, and Mono/Xamarin** . **Includes both client and listener** for peer-to-peer and broker-based messaging . **A more compact version for NETMF** available in AmqpNetMicro package . **For .NET Core**, separate packages for Core, Serialization, and WebSockets .

- **[ActiveMQ](https://activemq.apache.org/)**  
  **The most popular and powerful open-source Message Broker** (Apache-2.0) . **Supports cross-language clients** from Java, C#/.NET, C, C++, Ruby, Python, Perl, and PHP . **Multiple protocols**: OpenWire, STOMP, REST, Ajax/Cometd, XMPP . Features **Message Groups, Exclusive Queues, Master/Slave, Networks of Brokers** . Architecture based on **Message Brokers running on the network** acting as message router and optional persistence store .

- **[typedkafka](https://pypi.org/project/typedkafka/)**  
  **Fully type-hinted Kafka client for Python** (PyPI) . Built on **confluent-kafka** for performance . Features **full type hints and comprehensive docstrings**, **JSON/string/bytes message helpers**, **transaction support with context managers**, **async producer and consumer (asyncio)**, **retry utilities with exponential backoff**, **pluggable serializer framework** (JSON, String, Avro/Schema Registry), **testing utilities** (MockProducer/MockConsumer), and **type-safe configuration builders** . Requires **Python 3.9+** .

### Additional Strong Open-Source Options

- **[Streamix Queue](https://pypi.org/project/streamix-queue/)** — Lightweight Redis Streams event messenger for service-to-service communication . Features **consumer groups**, **automatic retries with exponential backoff**, **dead-letter queue**, and **stale message recovery** . Minimal dependencies (only Redis client) .
- **[beanq](https://pkg.go.dev/github.com/retail-ai-inc/beanq/v4)** — Go messaging library with **time-based scheduling**, **priority levels (0-999)**, **lock-based ordering**, **workflow with rollback support**, and **Redis hash status synchronization** . Supports **scaling consumers** via Docker .
- **[RabbitMQ](https://www.rabbitmq.com/)** — The open-source message broker itself (MPL-2.0) . **Interoperable** (AMQP 1.0 and MQTT 5.0), **flexible** (routing, filtering, streaming, federation), **reliable** (acknowledgements, cluster replication) . Use cases: decoupling services, RPC, streaming, IoT .
- Community **n8n** workflows for message queue integration and event routing automation.

**Frameworks for building custom systems**: Combine **Pika** or **Kombu** for Python AMQP messaging with **Celery** for distributed task queuing, **rabbitmq-client** for Node.js services, **AMQPNetLite** for .NET integration, and **ActiveMQ** or **RabbitMQ** as the broker—creating a fully self-hosted, enterprise-grade messaging platform.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- AMQP client libraries and message brokers handling application data must comply with data protection regulations (GDPR, CCPA, etc.) and follow secure messaging practices.
- **Pika is the pure-Python AMQP 0-9-1 reference implementation.** It supports multiple connection adapters (BlockingConnection, SelectConnection, AsyncioConnection, GeventConnection, TornadoConnection, TwistedProtocolConnection) and is used by AWS for Amazon MQ . **The standard choice for Python RabbitMQ integration.**
- **Kombu provides the high-level abstraction.** It supports pluggable transports, automatic serialization/compression, and graceful error handling . **Celery is built on Kombu** and is the standard Python task queue .
- **RabbitMQ 4.3 brings significant AMQP 1.0 improvements.** Rejected-by and Rejection Reason give publishers queue-specific failure details; Consumer Activity Notification signals link state via AMQP 1.0 flow frames . **VMware Tanzu RabbitMQ adds JMS queue type, message selectors, Queue Browser, and Spark Connector** .
- **Cloud messaging services have distinct architectures.** Amazon SQS is queue-focused with standard and FIFO variants . Azure Service Bus adds topics, sessions, and transactions . Google Cloud Pub/Sub supports push/pull, BigQuery, and Cloud Storage subscriptions . **Choose based on your existing cloud and messaging patterns.**
- Self-hosted open-source solutions require proper security hardening, connection management, and ongoing maintenance. **Message queues are critical infrastructure**—plan for high availability, monitoring, and disaster recovery.

---

**Made for developers, platform teams, and architects building transparent messaging solutions.**  
Let's make AMQP Client Libraries more open, data-driven, and reliable.
