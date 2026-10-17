# Uttam Kumar

**Backend & Platform Engineer · Java · Go**

I build Java/Spring Boot services and the integrations between systems: REST APIs, authentication, webhooks, and token lifecycles. My current focus is Go, distributed systems, and cloud-native engineering.

Bengaluru, India · [Selected work](#selected-engineering-work) · [Contact](#contact)

---

## Engineering experience

My professional backend work includes:

- **Services and APIs:** Java/Spring Boot development, REST endpoints, and application workflows.
- **Integrations:** third-party APIs, webhook handling, and workflows that connect external services.
- **Identity and access:** authentication, authorization, and token lifecycle handling.

I approach reliability through clear API contracts, explicit failure states, and service boundaries that remain understandable as requirements change.

## Selected engineering work

### [SpeakBetter](https://github.com/uttamkumar37/SpeakBetter)

*Personal application · in development · Java 21, Spring Boot, PostgreSQL, React/TypeScript*

Makes speaking and interview practice repeatable through recorded attempts, self-review, and practice history. The backend separates recording storage from session metadata, uses Flyway migrations, and schedules retention cleanup. Public test source covers upload validation, partial-content playback, and expiry behavior.

[Storage interface](https://github.com/uttamkumar37/SpeakBetter/blob/main/backend/src/main/java/com/speakbetter/practice/service/storage/RecordingStorage.java) · [API and integration tests](https://github.com/uttamkumar37/SpeakBetter/blob/main/backend/src/test/java/com/speakbetter/practice/controller/PracticeSessionIntegrationTest.java)

### [GenAI-Engineering](https://github.com/uttamkumar37/GenAI-Engineering)

*Learning lab · examples and design exercises · Python, Java/Spring AI*

Explores how model-backed features fit into backend systems. Examples cover bounded async concurrency, provider fallback, and circuit breakers. A Java/Python architecture exercise weighs service ownership against the latency and operational cost of another service.

[Provider client example](https://github.com/uttamkumar37/GenAI-Engineering/blob/main/code/01-python-for-ai/03-advanced/llm_provider_abstraction/client.py) · [Java/Python design exercise](https://github.com/uttamkumar37/GenAI-Engineering/blob/main/code/20-java-integration/03-advanced/java-python-hybrid-architecture/ARCHITECTURE.md)

### [System-Design](https://github.com/uttamkumar37/System-Design)

*Study curriculum · documented · distributed systems, databases, messaging*

A structured reference for reasoning from requirements to architecture. The curriculum examines consistency, caching, delivery guarantees, resilience, and observability, with URL-shortener and chat-system study prompts. The focus is making requirements and failure modes explicit before selecting components.

[Read the curriculum](https://github.com/uttamkumar37/System-Design/blob/main/system-design-curriculum.md)

**Also building:** CloudCampus, a multi-tenant school ERP SaaS project being rebuilt backend-first. It is in development, with private source.

## Architecture and engineering decisions

- **Keep storage replaceable.** SpeakBetter's [architecture notes](https://github.com/uttamkumar37/SpeakBetter#architecture-notes) explain local file streaming versus R2 playback through presigned URLs. The storage interface supports both without embedding storage details in the session workflow.
- **Make lifecycle rules testable.** The [retention tests](https://github.com/uttamkumar37/SpeakBetter/blob/main/backend/src/test/java/com/speakbetter/practice/controller/PracticeSessionIntegrationTest.java#L199) check that expired recordings are removed while unexpired recordings remain. Scheduled deletion needs an explicit expiry boundary.
- **Justify a service boundary.** The [Java/Python design exercise](https://github.com/uttamkumar37/GenAI-Engineering/blob/main/code/20-java-integration/03-advanced/java-python-hybrid-architecture/ARCHITECTURE.md) keeps business rules in Java and model-heavy work in Python, while acknowledging that a small feature may be simpler in one process.

## Technical expertise

- **Production experience:** Java, Spring Boot, REST APIs, third-party integrations, authentication and authorization, webhooks, token lifecycles.
- **Hands-on project work:** PostgreSQL, Flyway, Spring Data JPA, local/R2 storage adapters, React/TypeScript, Python learning examples, containerized local development.
- **Current learning and focus:** Go backend services and microservices, Podman, Kubernetes/OpenShift, distributed systems, and platform engineering.

## Technical writing and learning

I keep public study material alongside implementation exercises:

- [Backend-Notes](https://github.com/uttamkumar37/Backend-Notes) — introductory Java/Go practice, backend topics, and language roadmaps.
- [GenAI theory notes](https://github.com/uttamkumar37/GenAI-Engineering/tree/main/theory) — topic-based reading on retrieval, evaluation, reliability, and Java integration.

## Contact

[GitHub](https://github.com/uttamkumar37) · [LinkedIn](https://www.linkedin.com/in/uttamkumar37/) · [Email](mailto:uttamkumar3797@gmail.com)

If you're working on backend integrations, service boundaries, or platform tooling, I'd welcome a technical conversation.
