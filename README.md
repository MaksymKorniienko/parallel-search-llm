## System Architecture & UML Models

### 1. Use Case Diagram
Describes user and administrative interactions alongside the external LLM actor.

![Use Case Diagram](docs/images/Use%20Case%20Diagram.drawio.png)

---

### 2. Class Diagram
Outlines the core C++ architectural components, including concurrency primitives, thread pooling, sharded index storage, and network handlers.

![Class Diagram](docs/images/Class%20Diagram%20(C++).drawio.png)

---

### 3. Sequence Diagrams

#### A. Parallel Indexing Pipeline
Illustrates dataset distribution across worker threads and lock-striped mutations on the inverted index.

![Sequence - Parallel Indexing](docs/images/Sequence%20-%20Parallel%20Indexing.drawio.png)

#### B. WebSocket Real-Time Search
Details full-duplex communication and progressive stage notifications during query expansion and term retrieval.

![Sequence - WebSocket Search](docs/images/Sequence%20-%20WebSocket%20Search.drawio.png)

#### C. REST API Endpoints Lifecycle
Captures synchronous Request-Response lifecycles for `/api/health`, `/api/stats`, and `/api/search`.

![Sequence - REST API Endpoints](docs/images/Sequence%20-%20REST%20API%20Endpoints.drawio.png)

---

### 4. Deployment Diagram
Demonstrates the container topology, bridged Docker network, volume mounts, and port forwarding between the host system and service containers.

![Deployment Diagram](docs/images/Deployment%20Diagram%20(Docker).drawio.png)
