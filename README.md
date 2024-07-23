# Comparative Analysis of REST and gRPC Architectures

This repository contains the results and analysis of tests comparing the performance of REST and gRPC communication architectures. The tests were conducted using three main metrics: response time, CPU usage, and memory consumption.

## Test Specifications

The tests were conducted using Docker containers with the following configuration:
- CPU: 1 core (up to 2 cores)
- RAM: 1 GB
- Host Machine: Ryzen 5 3600X, 32 GB RAM, Windows 10

Two scenarios were tested for each architecture: 
1. 20 users
2. 100 users

Each test involved multiple requests over a period of 1 minute, and the metrics were collected and analyzed.

## Test Results

### Test 1: Fetching Few Records

#### 20 Users

- **Response Time**: The gRPC architecture showed a significantly lower average response time (1.34 ms) compared to REST (31.84 ms).
![Response Time - 20 Users](images/getone-20-response-time.png)
- **CPU Usage**: gRPC had a lower average CPU usage (28.11%) compared to REST (60.91%).
![CPU Usage - 20 Users](images/getone-20-cpu.png)
- **Memory Usage**: gRPC also had a lower average memory consumption (25.56 MB) compared to REST (30.34 MB).
![Memory Usage - 20 Users](images/getone-20-ram.png)

#### 100 Users

- **Response Time**: The average response time for gRPC remained significantly lower (1.38 ms) compared to REST (167.20 ms).
![Response Time - 100 Users](images/getone-100-response-time.png)
- **CPU Usage**: gRPC continued to use less CPU (28.99%) compared to REST (61.11%).
![CPU Usage - 100 Users](images/getone-100-cpu.png)
- **Memory Usage**: gRPC had lower memory usage (28.32 MB) compared to REST (73.08 MB).
![Memory Usage - 100 Users](images/getone-100-ram.png)

### Test 2: Fetching Many Records

#### 20 Users

- **Response Time**: The average response time for gRPC (105.29 ms) was lower compared to REST (347.75 ms).
![Response Time - 20 Users](images/getall-20-response-time.png)
- **CPU Usage**: gRPC had a lower average CPU usage (65.89%) compared to REST (74.76%).
![CPU Usage - 20 Users](images/getall-20-cpu.png)
- **Memory Usage**: gRPC had lower memory consumption (63.33 MB) compared to REST (88.46 MB).
![Memory Usage - 20 Users](images/getall-20-ram.png)

#### 100 Users

- **Response Time**: The average response time for gRPC (24.4 ms) was significantly lower compared to REST (1911.6 ms).
![Response Time - 100 Users](images/getall-100-response-time.png)
- **CPU Usage**: gRPC used less CPU (27.43%) compared to REST (81.93%).
![CPU Usage - 100 Users](images/getall-100-cpu.png)
- **Memory Usage**: gRPC had lower memory consumption (60.68 MB) compared to REST (88.84 MB).
![Memory Usage - 100 Users](images/getall-100-ram.png)

### Test 3: Inserting Small Payload

#### 20 Users

- **Response Time**: The average response time for gRPC (527 ms) was lower compared to REST (1066.5 ms).
![Response Time - 20 Users](images/postone-20-response-time.png)
- **CPU Usage**: gRPC had a lower average CPU usage (83.5%) compared to REST (94.39%).
![CPU Usage - 20 Users](images/postone-20-cpu.png)
- **Memory Usage**: gRPC had lower memory consumption (29.93 MB) compared to REST (84.89 MB).
![Memory Usage - 20 Users](images/postone-20-ram.png)

#### 100 Users

- **Response Time**: The average response time for gRPC (1012 ms) was significantly lower compared to REST (7578 ms).
![Response Time - 100 Users](images/postone-100-response-time.png)
- **CPU Usage**: gRPC used less CPU (88.66%) compared to REST (96.78%).
![CPU Usage - 100 Users](images/postone-100-cpu.png)
- **Memory Usage**: gRPC had lower memory consumption (32.44 MB) compared to REST (94.4 MB).
![Memory Usage - 100 Users](images/postone-100-ram.png)

### Test 4: Inserting Large Payload

#### 20 Users

- **Response Time**: The average response time for gRPC (1037 ms) was lower compared to REST (1297.5 ms).
![Response Time - 20 Users](images/postall-20-response-time.png)
- **CPU Usage**: gRPC had a slightly higher average CPU usage (105.05%) compared to REST (104.74%).
![CPU Usage - 20 Users](images/postall-20-cpu.png)
- **Memory Usage**: gRPC had higher memory consumption (37.89 MB) compared to REST (32.72 MB).
![Memory Usage - 20 Users](images/postall-20-ram.png)

#### 100 Users

- **Response Time**: The average response time for gRPC (1080 ms) was significantly lower compared to REST (19501 ms).
![Response Time - 100 Users](images/postall-100-response-time.png)
- **CPU Usage**: gRPC used less CPU (101.65%) compared to REST (105.82%).
![CPU Usage - 100 Users](images/postall-100-cpu.png)
- **Memory Usage**: gRPC had lower memory consumption (36.89 MB) compared to REST (96.88 MB).
![Memory Usage - 100 Users](images/postall-100-ram.png)

## Conclusions

The results indicate that the gRPC architecture consistently outperforms REST in terms of response time, CPU usage, and memory consumption across all tested scenarios. This makes gRPC a better choice for applications requiring high performance and resource efficiency. However, other factors such as implementation complexity, compatibility, and specific project requirements should also be considered when choosing an architecture.

For more details, refer to the figures and data provided in the repository.
