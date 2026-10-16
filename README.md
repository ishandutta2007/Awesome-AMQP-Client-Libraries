# Awesome-AMQP-Client-Libraries

## Top AMQP Client Libraries Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on AMQP Protocol Implementations, Message Brokers & Client Library Abstractions*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **AMQP Client Libraries**. These tools enable developers to implement the Advanced Message Queuing Protocol across languages and frameworks—providing high-level abstractions for publishing, consuming, and routing messages through brokers like RabbitMQ, ActiveMQ, and cloud messaging services.

**Examples** include Kombu, Pika, Celery, RabbitMQ, Amazon SQS, Azure Service Bus, Redis Streams, Google Cloud Pub/Sub, ActiveMQ, and Qpid Proton.

**Open-source emphasis**: This section is heavily expanded with major active projects for self-hosting, protocol implementation, and open messaging infrastructure—ideal for developers, platform teams, and architects seeking transparent, vendor-independent message queuing.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global enterprise messaging middleware and cloud event queuing market is estimated at approximately $15B–$18B and is projected to surpass $30B by 2030, propelled by event-driven architectures, microservices, and asynchronous stream workloads. The sector is moderately concentrated at the hosted infrastructure layer—dominated by hyper-scaler cloud titans (AWS, Microsoft Azure, Google Cloud)—while maintaining high fragmentation in client implementations, niche protocol gateways, and polyglot open-source developer libraries.

## SaaS/Hosted Platforms

| Platform | Company Valuation / Revenue | Starting Pricing | Free Tier Limits | Description |
| :--- | :--- | :--- | :--- | :--- |
| **[Azure Service Bus](https://azure.microsoft.com/en-us/products/service-bus/)** | ~$3.1T Market Cap (Microsoft) / ~$245B Ann. Rev. | $0.05 per million operations (Standard tier base: ~$10/month + $0.05 per million operations) | $200 free credit valid for 30 days via Azure Free Account, plus 750 hours/month of standard B1S VM burstable services | Fully managed enterprise message broker with queues and pub/sub topics. Supports message sessions, FIFO guarantees, auto-forwarding, and dead-letter queues. |
| **[Google Cloud Pub/Sub](https://cloud.google.com/pubsub)** | ~$2.1T Market Cap (Alphabet) / ~$307B Ann. Rev. | $40.00 per TiB of message data ($0.04/GiB beyond the free tier) | 10 GiB of message ingestion and delivery data per month free forever | Asynchronous messaging service decoupling senders and receivers. Features pull/push subscriptions, BigQuery subscriptions, and Cloud Storage subscriptions. |
| **[Amazon SQS](https://aws.amazon.com/sqs/)** | ~$1.9T Market Cap (Amazon) / ~$575B Ann. Rev. | $0.40 per 1 million requests (Standard queues) / $0.50 per 1 million requests (FIFO queues) | 1,000,000 requests per month free forever under the AWS Free Tier | Fully managed distributed message queuing service for decoupling microservices, featuring standard queues (at-least-once delivery) and FIFO queues. |
| **[RabbitMQ Cloud (Tanzu)](https://www.rabbitmq.com/)** | ~$600B+ Market Cap (Broadcom / VMware Tanzu) / ~$51B Ann. Rev. | Starting at ~$0.20/hour (~$145/month) for entry managed production clusters | 30-day free trial on Tanzu Platform Cloud / VMware Cloud Services with evaluation limits | Commercial edition of RabbitMQ with enterprise-grade plugins, Raft-backed JMS queue type, Queue Browser, and Spark Connector. |
| **[Redis Cloud](https://redis.io/)** | ~$4B+ Valuation / ~$150M+ ARR | $5.00/month for Fixed 250MB plan (pay-as-you-go flexible starting tier) | 30 MB storage and 30 concurrent connections free forever (Free Tier plan) | Fully managed cloud service for Redis with Streams for event messaging, consumer groups, automatic retries, and dead-letter queues. |

## Open-Source GitHub Projects

| Project | Stars | Language / Ecosystem | License | Description |
| :--- | :--- | :--- | :--- | :--- |
| **[Celery](https://github.com/celery/celery)** | [![GitHub stars](https://img.shields.io/github/stars/celery/celery?style=social&color=white)](https://github.com/celery/celery/stargazers) | Python | BSD-3-Clause | Distributed Task Queue mediating between clients and workers. Supports RabbitMQ, Redis, Amazon SQS, and more as message transports. |
| **[RabbitMQ Server](https://github.com/rabbitmq/rabbitmq-server)** | [![GitHub stars](https://img.shields.io/github/stars/rabbitmq/rabbitmq-server?style=social&color=white)](https://github.com/rabbitmq/rabbitmq-server/stargazers) | Erlang | MPL-2.0 | The open-source message broker core server. Provides robust AMQP 0-9-1 and AMQP 1.0 protocol implementations, stream filtering, and federation. |
| **[streadway/amqp](https://github.com/streadway/amqp)** | [![GitHub stars](https://img.shields.io/github/stars/streadway/amqp?style=social&color=white)](https://github.com/streadway/amqp/stargazers) | Go | BSD-2-Clause | Original canonical Go client for AMQP 0.9.1. Provides low-level channel and connection primitives for high-performance messaging pipelines. |
| **[Pika](https://github.com/pika/pika)** | [![GitHub stars](https://img.shields.io/github/stars/pika/pika?style=social&color=white)](https://github.com/pika/pika/stargazers) | Python | BSD-3-Clause | The pure-Python implementation of the AMQP 0-9-1 protocol including RabbitMQ's extensions. Supports Blocking, Asyncio, Select, Gevent, and Tornado adapters. |
| **[amqplib](https://github.com/amqp-node/amqplib)** | [![GitHub stars](https://img.shields.io/github/stars/amqp-node/amqplib?style=social&color=white)](https://github.com/amqp-node/amqplib/stargazers) | JavaScript / Node.js | MIT | The standard AMQP 0-9-1 library and client for Node.JS with Promise and callback based APIs. |
| **[Kombu](https://github.com/celery/kombu)** | [![GitHub stars](https://img.shields.io/github/stars/celery/kombu?style=social&color=white)](https://github.com/celery/kombu/stargazers) | Python | BSD-3-Clause | AMQP messaging framework for Python powering Celery. Provides an idiomatic high-level interface with pluggable transports, serialization, and compression. |
| **[ActiveMQ Classic](https://github.com/apache/activemq)** | [![GitHub stars](https://img.shields.io/github/stars/apache/activemq?style=social&color=white)](https://github.com/apache/activemq/stargazers) | Java | Apache-2.0 | Apache ActiveMQ message broker supporting multi-protocol messaging including AMQP 1.0, OpenWire, STOMP, MQTT, and cross-language clients. |
| **[rabbitmq/amqp091-go](https://github.com/rabbitmq/amqp091-go)** | [![GitHub stars](https://img.shields.io/github/stars/rabbitmq/amqp091-go?style=social&color=white)](https://github.com/rabbitmq/amqp091-go/stargazers) | Go | BSD-2-Clause | Official AMQP 0-9-1 Go client actively maintained by the RabbitMQ team, successor to `streadway/amqp`. |
| **[rabbitmq-c](https://github.com/alanxz/rabbitmq-c)** | [![GitHub stars](https://img.shields.io/github/stars/alanxz/rabbitmq-c?style=social&color=white)](https://github.com/alanxz/rabbitmq-c/stargazers) | C | MIT | C-language AMQP client library for use with AMQP 0-9-1 implementing brokers like RabbitMQ. |
| **[ActiveMQ Artemis](https://github.com/apache/activemq-artemis)** | [![GitHub stars](https://img.shields.io/github/stars/apache/activemq-artemis?style=social&color=white)](https://github.com/apache/activemq-artemis/stargazers) | Java | Apache-2.0 | Next-generation asynchronous high-performance messaging broker from Apache supporting AMQP, MQTT, STOMP, and JMS 2.0. |
| **[AMQPNetLite](https://github.com/azure/amqpnetlite)** | [![GitHub stars](https://img.shields.io/github/stars/azure/amqpnetlite?style=social&color=white)](https://github.com/azure/amqpnetlite/stargazers) | C# / .NET | MIT | Lightweight AMQP 1.0 library for .NET platforms including .NET Core, Framework, UWP, and Mono for peer-to-peer and broker messaging. |
| **[Qpid Proton](https://github.com/apache/qpid-proton)** | [![GitHub stars](https://img.shields.io/github/stars/apache/qpid-proton?style=social&color=white)](https://github.com/apache/qpid-proton/stargazers) | C / C++ / Python | Apache-2.0 | High-performance, lightweight AMQP 1.0 messaging library from Apache designed for integration in microservices, brokers, and routers. |
| **[rabbitmq-client (Node.js)](https://github.com/cody-greene/node-rabbitmq-client)** | [![GitHub stars](https://img.shields.io/github/stars/cody-greene/node-rabbitmq-client?style=social&color=white)](https://github.com/cody-greene/node-rabbitmq-client/stargazers) | TypeScript / Node.js | MIT | TypeScript-written client library for RabbitMQ with automatic reconnect, retry publishing, consumer/publisher abstractions, and zero dependencies. |
| **[beanq](https://github.com/retail-ai-inc/beanq)** | [![GitHub stars](https://img.shields.io/github/stars/retail-ai-inc/beanq?style=social&color=white)](https://github.com/retail-ai-inc/beanq/stargazers) | Go | MIT | Go job queue library featuring time-based scheduling, priority levels, rollback support, and dashboard monitoring. |

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- AMQP client libraries and message brokers handling application data must comply with data protection regulations (GDPR, CCPA, etc.) and follow secure messaging practices.
- **Pika is the pure-Python AMQP 0-9-1 reference implementation.** It supports multiple connection adapters (BlockingConnection, SelectConnection, AsyncioConnection, GeventConnection, TornadoConnection, TwistedProtocolConnection) and is used by AWS for Amazon MQ. **The standard choice for Python RabbitMQ integration.**
- **Kombu provides the high-level abstraction.** It supports pluggable transports, automatic serialization/compression, and graceful error handling. **Celery is built on Kombu** and is the standard Python task queue.
- **RabbitMQ 4.3 brings significant AMQP 1.0 improvements.** Rejected-by and Rejection Reason give publishers queue-specific failure details; Consumer Activity Notification signals link state via AMQP 1.0 flow frames. **VMware Tanzu RabbitMQ adds JMS queue type, message selectors, Queue Browser, and Spark Connector**.
- **Cloud messaging services have distinct architectures.** Amazon SQS is queue-focused with standard and FIFO variants. Azure Service Bus adds topics, sessions, and transactions. Google Cloud Pub/Sub supports push/pull, BigQuery, and Cloud Storage subscriptions. **Choose based on your existing cloud and messaging patterns.**
- Self-hosted open-source solutions require proper security hardening, connection management, and ongoing maintenance. **Message queues are critical infrastructure**—plan for high availability, monitoring, and disaster recovery.

---

**Made for developers, platform teams, and architects building transparent messaging solutions.**  
Let's make AMQP Client Libraries more open, data-driven, and reliable.
