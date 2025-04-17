# Real-Time Kafka Debezium Data Pipeline

This project demonstrates a real-time data streaming pipeline using **MySQL**, **Debezium**, **Kafka**, and **Docker Compose**.

## 🚀 Project Overview

The pipeline enables real-time change data capture (CDC) from MySQL and streams the changes to Kafka topics using Debezium.

### ✅ Technologies Used
- MySQL
- Debezium
- Apache Kafka
- Docker Compose
- Kafka Connect

---

## 📁 Project Structure

```
real-time-kafka-debezium-pipeline/
│
├── docker-compose.yaml     # Orchestrates all containers
├── sql/
│   └── init.sql            # Initializes MySQL DB and tables
└── README.md               # Project documentation
```

---

## 🛠️ How to Run the Project

1. Clone or upload this repo.
2. Open terminal in the root folder.
3. Run:

```bash
docker-compose up
```

4. MySQL, Kafka, Zookeeper, and Kafka Connect will start.
5. MySQL will auto-create the `inventory` database and `products` table from `init.sql`.

---

## 🔄 Real-Time Data Flow

1. Data inserted/updated in MySQL gets logged in binary log.
2. Debezium reads MySQL binlogs.
3. Debezium publishes changes as Kafka topics in JSON format.
4. Kafka consumers can subscribe to these topics.

---

## 📦 Example Kafka Topic

Once running, changes in the MySQL `products` table will appear in:

```
dbserver1.inventory.products
```

---

## 🧠 Key Learnings

- Kafka architecture and topics
- Change Data Capture with Debezium
- Connecting Kafka with MySQL via Debezium
- Docker-based orchestration of services

---

## 📌 Challenges Faced

- Schema evolution and breaking changes
- Container networking issues
- Kafka connector configurations
- Latency in syncing under heavy loads

---

## 📬 Contact

Built by **Srikar Maadhu**  
Email: srikar.maadhusrikar@gmail.com 
