# Research open-source vector databases for RAG · research (revision)

**TL;DR:** Qdrant and Weaviate are strong open-source vector database options for a small RAG app, with Qdrant leading in single-thread speed and low latency for RAG applications.

## Answer

For a small RAG application, the leading open-source vector database choices are **Qdrant** and **Weaviate**, each offering distinct advantages depending on specific needs such as hybrid search, ease of deployment, and metadata filtering. Qdrant is particularly noted for its speed, Rust-based architecture, and strong metadata filtering capabilities, making it ideal for lightweight, fast, and easy-to-operate deployments. Weaviate excels in scenarios requiring native hybrid search (combining keyword and vector search) and offers built-in embedding modules, simplifying the insertion of raw text without managing separate embedding pipelines.

## Key findings

- **Performance**: Qdrant leads in single-thread speed and low latency, critical for RAG applications, with independent 2026 benchmarks showing consistently low query latencies. 
- **Ease of Use**: Both Qdrant and Weaviate are noted for their ease of setup and use, particularly for prototyping and quick deployment.
- **Scalability**: While Qdrant is recommended for small-scale applications, Milvus is better suited for billion-scale workloads with distributed, Kubernetes-native architecture. 
- **Hybrid Search**: Weaviate supports native hybrid search, combining vector similarity with keyword matching, essential for nuanced retrieval in RAG systems.
- **Metadata Filtering**: Both Qdrant and Weaviate support strong metadata filtering, enabling precise and contextually relevant retrievals.
- **Deployment**: Qdrant and Weaviate are both compatible with single-box self-hosting, aligning with the team's requirement for a one-box deployment.
- **Cost/Operations**: All mentioned databases are open-source, but considerations for hosting, support costs, and operational overhead should be evaluated. Qdrant and Weaviate are noted for their relatively low operational complexity compared to Milvus, which is more resource-intensive.

## Implications for the team

- **Start with Qdrant** for its balance of performance, ease of deployment, and filtering capabilities, which align well with the requirements of a small RAG application. 
- **Consider Weaviate** if hybrid search capabilities are critical or if the team prefers built-in embedding modules to simplify the pipeline. 
- Evaluate existing infrastructure and team capacity for operational tasks, as self-hosting Qdrant or Weaviate requires internal support and monitoring. 
- Prototype with both options to validate concepts before transitioning to a more scalable solution if needed.

## Open questions

- **DECISION: Does the team need hybrid search (keyword + vector)?** If yes, Weaviate is preferred; if no, Qdrant is lighter and faster. 
- **DECISION: What are the specific metadata filtering requirements for the RAG application?** This will influence whether Qdrant or Weaviate’s filtering capabilities are more suitable. 
- **DECISION: What existing infrastructure is available?** If PostgreSQL is already in use, pgvector could be considered, though it may not scale as efficiently as dedicated solutions. 
- **DECISION: How will the chosen database handle increasing data volumes and query loads as the application scales?** This will guide whether Qdrant’s current capabilities will suffice or if planning for Milvus’s scalability is necessary. 
- **DECISION: What are the team’s operational capabilities?** Determine if the team can manage self-hosted solutions like Qdrant or Weaviate, or if a managed service might be more appropriate.

### Checked by Anchor
Read 3 source pages in a cloud browser. Groundedness 0.75: Most factual claims about vector database characteristics are well-supported by the source pages (Qdrant's Rust-based architecture, single-thread speed, metadata filtering; Weaviate's hybrid search and embedding modules; Milvus for billion-scale). However, some claims lack direct support: the specific reference to "independent 2026 benchmarks" for Qdrant's latency is mentioned in sources but not detailed enough to fully verify the claim's scope, and the claim about pgvector being "a pragmatic choice if you already run Postgres" appears only in SOURCE PAGE 2's counterargument section, not in primary recommendations. SOURCE PAGE 3 is irrelevant (Bitcoin mining content).

## Sources
- [stork.ai](https://www.stork.ai/blog/best-open-source-vector-databases-2026) (read by Anchor)
- [markaicode.com](https://markaicode.com/best/best-vector-database-2026/) (read by Anchor)
- [d-central.tech](https://d-central.tech/self-hosted-vector-databases/) (read by Anchor)
