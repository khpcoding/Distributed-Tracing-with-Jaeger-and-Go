# Distributed Tracing with Jaeger and OpenTracing

This project demonstrates distributed tracing in a microservices architecture using **Jaeger** and **OpenTracing**. It consists of three services (`Service A`, `Service B`, and `Service C`) that communicate with each other, and traces are collected and visualized using Jaeger.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Technologies Used](#technologies-used)
3. [Prerequisites](#prerequisites)
4. [Setup and Installation](#setup-and-installation)
5. [Running the Project](#running-the-project)
6. [Viewing Traces in Jaeger UI](#viewing-traces-in-jaeger-ui)
7. [Project Structure](#project-structure)
8. [License](#license)

---

## Project Overview

This project simulates a microservices environment where:
- **Service A** calls **Service B**.
- **Service B** calls **Service C**.
- Each service is instrumented with **OpenTracing** to generate traces.
- Traces are collected and visualized using **Jaeger**.

The project also includes a **Docker Compose** setup to run Jaeger, Elasticsearch, and Kibana for trace storage and visualization.


![1_arc](https://github.com/user-attachments/assets/2f713118-07ce-4a63-a3ee-c9f5e61d3b29)



---

## Technologies Used

- **Go** (Golang) for building microservices.
- **OpenTracing** for distributed tracing.
- **Jaeger** for trace collection and visualization.
- **Docker Compose** for container orchestration.
- **Elasticsearch** for trace storage.
- **Kibana** for log visualization (optional).

---

## Prerequisites

Before running the project, ensure you have the following installed:

1. **Docker** and **Docker Compose**:
   - [Install Docker](https://docs.docker.com/get-docker/)
   - [Install Docker Compose](https://docs.docker.com/compose/install/)

2. **Go** (optional, if you want to run the services locally without Docker):
   - [Install Go](https://golang.org/doc/install)

---

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/khpcoding/Distributed-Tracing-with-Jaeger-and-Go.git
   cd Distributed-Tracing-with-Jaeger-and-Go
   ```
---

## This will start the following services:

  - Jaeger (UI at http://localhost:16686)

  - Elasticsearch (for trace storage)

  - Kibana (optional, for log visualization at http://localhost:5601)

  - Service A, Service B, and Service C.

---
## Running the Project

Once the services are up and running, you can interact with them as follows:

1- Service A is available at http://localhost:8080/service-a.

2- Service B is available at http://localhost:8081/service-b.

3- Service C is available at http://localhost:8082/service-c.

To trigger a trace, simply make a request to Service A:

```bash
curl http://localhost:8080/service-a
```
This will initiate a chain of requests:

Service A → Service B → Service C.

---

Viewing Traces in Jaeger UI

1- Open the Jaeger UI in your browser:

```bash
http://localhost:16686
```
2- Search for traces by selecting the service name (serviceA, serviceB, or serviceC) and clicking Find Traces.

3- You can visualize the entire request flow, including the time taken by each service and the relationships between them.

![image](https://github.com/user-attachments/assets/82f388e5-2294-44de-a0f0-c6c5c4928519)


![image](https://github.com/user-attachments/assets/ff7ac7d3-8206-4a85-b26e-fea768e74270)

