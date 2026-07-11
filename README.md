
# 💳 Offline Payment System App

An experimental Spring Boot + MongoDB application that simulates **offline-first payments** using a Bluetooth mesh-style network.  
Packets (representing transactions) can hop across nearby devices until they reach a bridge node with internet access, which then uploads them securely to the backend.

---

## 🚀 Features
- **Mesh Networking Simulation**: Devices gossip encrypted payment packets across the network.
- **Bridge Uploads**: Packets reaching a device with internet are flushed to the backend.
- **End-to-End Encryption**: Transactions are encrypted with the bank’s public key, ensuring privacy even when relayed by strangers.
- **Offline-First Design**: Payments can be initiated without internet and still reach the bank eventually.
- **Resettable Mesh**: Clear all packets and start fresh for testing scenarios.

---

## 🛠️ Tech Stack
- **Java 17**
- **Spring Boot**
- **Spring Data MongoDB**
- **JUnit 5** (for integration tests)
- **Docker / Testcontainers** (optional, for isolated DB testing)

---

## 📦 Getting Started

### Prerequisites
- Java 17+
- Maven 3.8+
- MongoDB (local or Docker)
- Docker (optional, for Testcontainers)

### Installation
```bash
# Clone the repository
git clone https://github.com/your-username/offline-payment-system.git
cd offline-payment-system

# Build the project
mvn clean install

# Run the app
mvn spring-boot:run
