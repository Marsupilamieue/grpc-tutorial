Faris Zhafir Faza

2206081931

1. What are the key differences between unary, server streaming, and bi-directional streaming RPC (Remote Procedure Call) methods, and in what scenarios would each be most suitable?

    - Unary: This involves a single request from the client to the server, which then processes the request and returns a single response. It's suitable for simple client-server interactions where a single piece of data is exchanged.
    - Server streaming: The server sends back a stream of data to the client in response to a single request. This is useful when the server needs to send a potentially large or indefinite amount of data to the client, such as in real-time updates or data feeds.
    - Bidirectional streaming: Both the client and server establish a persistent connection and can send a stream of messages to each other concurrently. This is ideal for scenarios like chat applications or multiplayer gaming, where both sides need to send and receive data asynchronously.

2. What are the potential security considerations involved in implementing a gRPC service in Rust, particularly regarding authentication, authorization, and data encryption?

    - Authentication: Ensuring that only authorized clients can access gRPC service.
    - Authorization: Controlling what authenticated clients are allowed to do within the service.
    - Data Encryption: Encrypting data in transit to protect it from unauthorized access.

3. What are the potential challenges or issues that may arise when handling bidirectional streaming in Rust gRPC, especially in scenarios like chat applications?

    - Concurrency management: Ensuring that concurrent streams of data are handled correctly and efficiently.
    - Error handling: Dealing with errors that may occur asynchronously on either the client or server side.

4. What are the advantages and disadvantages of using the tokio_stream::wrappers::ReceiverStream for streaming responses in Rust gRPC services?

    - Advantages: It allows to easily convert a tokio Receiver into a Stream, which can simplify handling streaming responses in Rust gRPC services.
    - Disadvantages: It may introduce additional complexity if not used carefully, especially in scenarios with high concurrency or complex stream processing requirements.

5. In what ways could the Rust gRPC code be structured to facilitate code reuse and modularity, promoting maintainability and extensibility over time?

    - Organize code into reusable components and modules, separating concerns such as request handling, business logic, and data access.
    - Use traits and generics to abstract over different implementations and promote code reuse.

6. In the MyPaymentService implementation, what additional steps might be necessary to handle more complex payment processing logic?
    - Implement transaction handling and validation to ensure the integrity and security of payment transactions.
    - Incorporate error handling and logging to track and troubleshoot payment-related issues.
    - Consider integrating with external payment gateways or services for processing actual payments.

7. What impact does the adoption of gRPC as a communication protocol have on the overall architecture and design of distributed systems, particularly in terms of interoperability with other technologies and platforms?

    - gRPC promotes a more efficient and scalable communication protocol compared to traditional REST APIs.
    - It facilitates interoperability between services written in different languages and running on different platforms.
    - However, it may require additional tooling and infrastructure to support, especially in legacy systems.

8. What are the advantages and disadvantages of using HTTP/2, the underlying protocol for gRPC, compared to HTTP/1.1 or HTTP/1.1 with WebSocket for REST APIs?

    - Advantages of HTTP/2: Multiplexing, header compression, server push, and better support for bidirectional communication compared to HTTP/1.1 or WebSocket.
    - Disadvantages: Complexity and potential compatibility issues with older systems or proxies that don't fully support HTTP/2.

9. How does the request-response model of REST APIs contrast with the bidirectional streaming capabilities of gRPC in terms of real-time communication and responsiveness?

    - REST APIs follow a request-response model where clients send requests and wait for responses, which may not be suitable for real-time communication or scenarios requiring bidirectional data flow.
    - gRPC's bidirectional streaming capabilities allow for more responsive and interactive communication, making it better suited for real-time applications like chat or collaborative editing.

10. What are the implications of the schema-based approach of gRPC, using Protocol Buffers, compared to the more flexible, schema-less nature of JSON in REST API payloads?

    - gRPC's schema-based approach using Protocol Buffers provides strong typing and automatic code generation, which can help catch errors at compile time and improve performance.
    - However, it may be less flexible than JSON in terms of supporting dynamic or evolving data structures, especially in loosely coupled systems with heterogeneous payloads.