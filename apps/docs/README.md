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

## DevOps

### AWS Services (Good to know)

Aws is a cloud provider - have over 200 services.

**EC2 :** Simple VM like cloud service.

**EBS :** Simple long term data storage, durable with accessbility features. (Volume)

**S3 :** Simple Storage.(Storage)

**IAM :** (Identity and Access Management)

**CloudWatch :** Monitoring in AWS

**LAMBDA :** Serverless Compute. Sends mail and notification. Used for short actions. Do not need to deploy anything to it. Some functions provided by aws to make things easier.

Can create 100s of machines and clusters with one command.

**Cloud Build Services :** You can do CI/CD using Jenkins.

But AWS provides us with some alternative to these:

- CodePipline :
- CodeBuild : Compile code, run tests
- CodeDeploy : Deploying on EC2 and own premises.

**AWS Configuration :** Configure the things after they have been setup. Fill in the nitty gritty.

**Billing & Costing :** How much your organization is spending on services.

**AWS KMS :** Key Management Service. Key,Certificates (Same thing)

**Cloud Trail :** Logs the event that happen or the opeation that took place.

**EKS :** Similar to Kubernetes on AWS cloud. Orchestration software

**Fargate, ECS :**

EKs and ECS are different as, ECS is proprietary service while, EkS is Managed Kubernetes Service

ELK: Elastic search log stash kibana. Fetches errors from different services. Logging Mechanism. Alternatives could be splunk. Prevents

# Git And Github

Branching Strategy:

The latest stable release should be in master/main branch

while branches of different releases should be tracked as well.

While working on some differnet and new feature a seprate branch should be started.

# Github Actions

An alternative to jenkins. But github specific.

This needs to be configured for the processes to be executed as per needs.

```
.github/workflows/actions.yml
```

There can be many .yml actions file as per needs.
