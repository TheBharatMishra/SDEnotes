# SDEnotes

Taking notes as learning about software development. Will keep adding to it.

## Serverless Computing

requires zero configuration and maintainance from the developer

Provides serverless functions. Gives rise to microservice architecture.

These functions trigger different events on cloud

- https
- firestore
- pubsub
- storage
- analytics

Can be deployed using single command.

## gRPC, tRPC, GraphQL or REST

**REST** is an architecture. Similar to object oriented programming. Easier to build.

Do not scale that well.

Overfetching and Underfetching are also a problem.

Use REST when you need to move fast.

**GraphQL** is a query language. Eliminates Overfetching and underfetching. Fetches Only the data we need. Daves bandwidth and prevents replication.

Requires scehma definition to be right. Otherwise bugs may occur.

GraphQL client libraries are pretty complex and requires boilerplate code.

For example: Apollo cache management system does not maps with the browsers cache management system.

### Use GraphQL when:

- Complex Data Representation
- Nested Routes
- Objects with a lot of inheritance
- Bandwidth is priority
- on edge devices, smartphones

### tRPC - typescript REMOTE PROCEDURAL CALL

Helps to bridge frontend and backend.
Mainly typescript projects.

Controllers work without any error.

Typescript is used for scehma definition.
Data validation is good.

It is common to use monorepo with tRPC.

It runs on over HTTP2. Is lightweight compared to GraphQL(much lower bundle size).

If you are using JS or TS on both client and server and it is better to use tRPC as compared to REST.

### gRPC - google REMOTE PROCEDURAL CALL

Works same as tRPC.
Doesnt work witb JSON. Own format ProtoBuffer.

Is faster compared to all the other ways.

Good for microservices. And when they are written in different languages.

RPC are a concept even before REST. gRPC is the most optimized implementation of it till now.
