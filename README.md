# Distributed Log Processing with Apache Kafka

An advanced implementation of real-time log processing using Apache Kafka's producer-consumer architecture, featuring consumer groups, load balancing, and fanout configurations for scalable data streaming.

## 🎯 Project Overview

This project demonstrates enterprise-level log processing capabilities using Apache Kafka to handle Nginx web server logs in real-time. The system implements multiple consumer patterns including fanout distribution and load balancing to showcase Kafka's flexibility in handling diverse data streaming requirements.

## 🛠️ Technologies Used

- **Apache Kafka** - Distributed event streaming platform
- **Apache Zookeeper** - Distributed coordination service
- **Python 3** - Application development with confluent-kafka library
- **Docker** - Containerized deployment (Confluent & Bitnami images)
- **Nginx Logs** - Real-world log data for testing

## 📋 Key Features

### Producer-Consumer Architecture
- Custom Python producer for streaming Nginx access logs
- Real-time message publishing to Kafka topics
- Asynchronous delivery confirmation with callbacks
- UTF-8 encoding for reliable text data handling

### Advanced Consumer Patterns
- **Fanout Configuration**: Multiple consumer groups independently processing same data stream
- **Load Balancing**: Distributed message processing across consumer group members
- **Partition Management**: Exclusive partition assignment for efficient data distribution

### System Capabilities
- Real-time log entry processing and monitoring
- Scalable message distribution across multiple consumers
- Fault-tolerant message delivery with acknowledgment
- Docker-based isolated deployment environments

## 🏗️ Architecture Comparison

Conducted comprehensive analysis comparing Kafka with other message brokers:

| Feature | Kafka | RabbitMQ | ActiveMQ | AWS SNS |
|---------|-------|----------|----------|---------|
| **Architecture** | Distributed, log-based | Centralized, queue-based | Centralized | Managed pub/sub |
| **Throughput** | Very high | Moderate | Moderate | High (AWS-dependent) |
| **Persistence** | Durable disk storage | Optional | Optional | No persistence |
| **Scalability** | Highly scalable with partitioning | Limited horizontal scaling | Limited | AWS-managed |
| **Ordering** | Guaranteed per partition | Optional | Configurable | No strict ordering |

## 💡 Implementation Highlights

### Producer Implementation
- Reads Nginx access logs from file system
- Publishes log entries to `nginx_logs` topic
- Implements delivery callbacks for reliability monitoring
- Handles UTF-8 encoding for international character support

### Consumer Configurations

**Fanout Setup:**
- Multiple consumer groups consuming identical data streams
- Each group processes complete dataset independently
- Ideal for parallel processing by different applications
- Demonstrated with separate group IDs (`fanout-group-1`, `fanout-group-2`)

**Load Balancing Setup:**
- Single consumer group with multiple members
- Kafka automatically distributes messages across consumers
- Enhances throughput and processing efficiency
- Perfect for high-volume data processing scenarios

### Docker Deployment
- Tested with both Confluent and Bitnami Kafka images
- Isolated Zookeeper and Kafka containers
- Network configuration for inter-container communication
- Port mapping for localhost accessibility

## 📊 Results & Validation

**Message Flow Verification:**
- Successfully created and managed Kafka topics
- Validated end-to-end message delivery from producer to consumers
- Confirmed fanout pattern with duplicate message delivery to all groups
- Demonstrated load balancing with distributed message processing

**Performance Observations:**
- Real-time log processing with minimal latency
- Reliable message delivery with confirmation callbacks
- Scalable architecture supporting multiple concurrent consumers
- Effective partition management for data distribution

## 🚀 Skills Demonstrated

- **Distributed Systems Architecture**: Message broker implementation and configuration
- **Stream Processing**: Real-time data pipeline development
- **Python Development**: Producer-consumer application development
- **Docker & Containerization**: Multi-container orchestration
- **System Integration**: Kafka-Zookeeper-Python ecosystem integration
- **Performance Optimization**: Load balancing and fanout patterns
- **Technical Analysis**: Comparative evaluation of message brokers

## 📄 Documentation

For detailed implementation steps, code samples, architecture diagrams, and technical analysis, see the [complete project documentation](kafka assignment.pdf).

## 🎓 Background

Developed this project to gain hands-on experience with enterprise-grade stream processing systems. Collaborated with peers to explore Kafka's advanced features including consumer groups, partition management, and various message distribution patterns used by companies like LinkedIn, Uber, and Netflix for their real-time data infrastructure.

## 🔗 Connect

**Meriem Lmoubariki**
- GitHub: [@myriamlmiii](https://github.com/myriamlmiii)

---

*This project demonstrates proficiency in distributed stream processing, message broker architectures, and scalable data pipeline design.*
