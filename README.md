# Redis Rate Limiter (Spring Boot)

Production-style Rate Limiter implemented using **Redis Token Bucket algorithm**
with **Spring Cloud Gateway**.

This project demonstrates how to build a distributed rate limiter
for microservices.

---

## Tech Stack
- Java 17 / 21
- Spring Boot
- Spring Cloud Gateway
- Redis
- Jedis
- Python (mock backend)

---

## Architecture Flow

Client  
→ Spring Cloud Gateway  
→ TokenBucketRateLimiterFilter  
→ Redis (Token Bucket)  
→ Mock Backend Server

---

## Screenshots

### Redis Server Running
![Redis](screenshot/redis-server img.png)

### Mock Python Server
![Mock](screenshot/python mock server img.png)

### Spring Boot Gateway
![Spring Boot](screenshot/springboot ing.png)

### Rate Limit Test Result
![Result](screenshot/Test result img.png)


## How to Run

### 1. Start Redis
Terminal 1:
```bash
redis-server

### 2. Start Mock Backend Server
Terminal 2:
python mock_server_simple.py

### 3. Start Spring Boot Gateway
Terminal 3:
mvn spring-boot:run

### 4. Test Rate Limiting
Terminal 4:
./quick-test.sh
