**Paypal Payment Integration Microservices – Parent Repository**

This repository contains a complete microservices-based payment gateway system implemented using Spring Boot and Eureka Service Discovery.
The architecture includes three independent microservices:

1.Eureka Server (Service Registry)

2.Payment Processing Service

3.PayPal Provider Service

**All services communicate dynamically using service name discovery, without any hard-coded URLs.
The processing service discovers the provider service through Eureka and calls its APIs to create and capture PayPal orders.**

**Description**

This parent repository demonstrates a real-world Payment Gateway Microservice Architecture. It showcases how microservices interact using Eureka Service Discovery and how payment operations are delegated to specialized services.

**🔹 Eureka Server**

Acts as the central service registry where all microservices register and discover each other dynamically.

**🔹 Payment Processing Service**

Responsible for handling payment workflows.
Instead of calling the provider service using a fixed URL, it uses service lookup through Eureka to locate:

**🔹 PayPal Provider Service**

Performs actual communication with PayPal APIs such as:
Create Order
Capture Order
It sends responses back to the processing service.
