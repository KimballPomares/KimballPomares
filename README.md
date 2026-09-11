I build ingestion and stream-processing systems in TypeScript, with an emphasis on durable queues, bounded workers, and operational clarity.
## @KimballPomares
I build ingestion and stream-processing systems in TypeScript, with an emphasis on durable queues, bounded workers, and operational clarity.
I own APIs, schemas, worker backpressure, and replay paths from source to durable storage.
My operational priorities are bounded failures, clear ownership, and recovery that does not depend on a person guessing the state.
I accept small duplication and conservative migrations over opaque abstractions that hide failure modes.
### 🛠 Tech & Infrastructure
- **Core:** `TypeScript`, `Node.js`
- **Data:** `PostgreSQL`, `Redis`, `Apache Kafka`
- **Infra:** `Docker`, `Kubernetes`, `Terraform`
- **Tooling:** `GitHub Actions`
### ⚙️ Engineering Areas
- Backpressure-aware workers that isolate poison records without losing replay context.
- Schema compatibility checks across APIs, Kafka topics, and PostgreSQL migrations.
- Trace propagation across RPCs, queues, and downstream storage calls.
- Deployment gates for lint, type checks, builds, and integration tests.
### 🔭 Current Focus
- Replacing unbounded queue consumers with per-partition concurrency limits.
- Testing Kafka replay against a frozen schema and snapshot without duplicating production state.
- Balancing compact PostgreSQL indexes against write amplification during bulk ingestion.
- Making retry classification explicit so transient failures do not mask permanent schema errors.
### 📌 Engineering Notes
- Tests should exercise boundaries: queue acknowledgements, schema changes, and worker restarts.
- Migrations need a forward-compatible writer before the reader changes.
- Error handling should preserve the record, correlation ID, and retry reason together.
- Deployments should fail loudly when lint, type checks, builds, or tests regress.
### 🧭 How I Work
- Prefer observable state and explicit ownership over hidden global assumptions.
- Keep failure modes recoverable before optimizing throughput.
[kimballpomares84@hotmail.com](mailto:kimballpomares84@hotmail.com)