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

T.B.D

### Achieving Loose Coupling in Communication

T.B.D
