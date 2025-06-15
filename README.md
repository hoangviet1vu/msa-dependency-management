# Dependency Management on Microservices

When working on Microservices System, we don't work with only single application, we work with a system that composed of multiple services (application), that each single service will have their own responsibility and have relationship with others that will make the service dependencies.
If with Object Oriented Programming, we have the strategy of `loose coupling, high cohesion` when designing classes relationship, we have the same with Microservices when designing Services with  consideration of what is the responsibility of the service, how is it constructed and how will the service communicate with others.

When working with a microservices system, we are no longer dealing with a single application, but with a distributed system composed of multiple services. Each service is responsible for a specific business function and must interact with others, forming a web of service dependencies. Just as object-oriented design promotes `loose coupling and high cohesion` between classes, the same principles apply to microservices. Designing effective services requires careful consideration of each service’s responsibility, how it is structured, and how it communicates with others.

##  Designing Cohesive and Loosely Coupled Services

Effective microservice architecture begins with thoughtful service design. A well-designed service must encapsulate a clear and focused responsibility, aligning with business domains and promoting high cohesion. At the same time, to enable scalability and maintainability, services must be loosely coupled — interacting through well-defined, minimal interfaces that reduce interdependencies.

This section explores two key aspects of service design:

- **Defining High-Cohesion Services:** How to structure services based on business context, domain boundaries, and the Single Responsibility Principle (SRP) from the SOLID design framework.

- **Achieving Loose Coupling in Communication:** How to design interactions between services to minimize dependencies, using patterns such as REST, gRPC, asynchronous messaging, and service mesh technologies.


### Defining High-Cohesion Services

When designing a microservice, one of the most important principles to follow is the **Single Responsibility Principle (SRP)** — the idea that each service should be responsible for a single, clearly defined task or business capability. In microservices architecture, this responsibility must be rooted in the **domain model** and the **business context** the service is intended to fulfill. A well-defined service should be simple, focused, and cohesive in purpose.

For core domain services, such as an Order Service in an e-commerce system, it is essential to maintain strict boundaries and data ownership. This can be achieved by applying the [**Database per Service pattern**](https://microservices.io/patterns/data/database-per-service.html). Under this pattern, each service is given exclusive access to its own database, ensuring that data is not shared directly between services. This approach enforces encapsulation and helps prevent data duplication and unintended side effects across services.

Take the **Order Service** as an example: it is responsible for managing the **Order domain**, which includes handling order records and order items. This service owns a dedicated **Order database**, which includes tables like `Orders` and `OrderItems`. When another service — such as the **Delivery Service** — needs information about an order (e.g., to initiate shipping), it does not access the Order database directly. Instead, it communicates with the Order Service through well-defined **RESTful APIs**.

![Order Service](./img/msa.drawio.png)

By enforcing this boundary, all CRUD operations on orders remain the sole responsibility of the Order Service. This guarantees **data integrity**, **service autonomy**, and ensures that no unexpected changes occur outside the knowledge of the owning service. In turn, this promotes a **high-cohesion** design that is easier to maintain, scale, and evolve independently.

### Achieving Loose Coupling in Communication

In a microservices architecture, how services communicate with each other plays a crucial role in determining the system’s flexibility, scalability, and maintainability. To achieve **loose coupling**, service interactions must be carefully designed to minimize direct dependencies, allowing each service to evolve independently without breaking others. This aligns closely with SOLID principles such as the **Dependency Inversion Principle**, **Interface Segregation Principle**, and **Open/Closed Principle**.

This section explores two main communication approaches and how they support the goal of loose coupling:

- **Synchronous Communication Approaches:**
This sub-section covers techniques such as RESTful APIs and gRPC, focusing on defining clear and minimal service interfaces using OpenAPI or Protocol Buffers. It also introduces the use of API versioning and the Sidecar pattern to abstract service interactions, enabling better control over routing, rate limiting, and fault tolerance.

- **Asynchronous Communication Approaches:**
This sub-section highlights the challenges of point-to-point messaging and explains how to reduce inter-service dependencies by adopting event-driven architecture using publish-subscribe patterns. It emphasizes designing topic-based communication channels that follow the Open/Closed Principle and promote scalability through loosely coupled event producers and consumers.

#### Synchronous Communication Approaches
T.B.D 

#### Asynchronous Communication Approaches
T.B.D
