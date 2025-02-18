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

   # This will start the following services:
  - Jaeger (UI at http://localhost:16686)

  - Elasticsearch (for trace storage)

  - Kibana (optional, for log visualization at http://localhost:5601)

  - Service A, Service B, and Service C.

