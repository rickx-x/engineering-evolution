# Master index

## How to use this repository

Follow a problem across time: identify the constraint that made the old design fail, read the original source, sketch the design, then write down what you would choose under today's constraints. A technology name is only a signpost; the useful unit of study is the problem and the trade-off.

## Historical orientation

- [Chronological timeline](TIMELINE.md)
- [Official engineering blog directory](BIG_TECH_BLOGS.md)
- [Engineering journal](../journal/README.md)

## Research tracks

### Backend & Distributed Systems

Monoliths and service boundaries · RPC and REST · asynchronous messaging · relational and non-relational data models · indexing and query plans · transactions and isolation · replication and consensus · partitioning and sharding · caching · CAP and consistency models · concurrency · networking · load balancing · resilience · identity and access control · cloud-native and serverless systems.

### Big Tech at Scale

Google search and storage · Amazon transactional systems and AWS · Meta social graph and ranking · Netflix content delivery and resilience · Uber marketplace and event processing · LinkedIn Kafka and data systems · Microsoft cloud and developer platforms · Apple device and service infrastructure · Cloudflare global edge · Stripe payment correctness · Airbnb marketplace/data · Spotify media and experimentation · Discord real-time communication · Shopify commerce · Pinterest discovery · Dropbox synchronization/storage · Reddit community-scale serving.

Each company chapter will separate publicly documented architecture from inference. Public articles are snapshots of particular systems and dates, not complete descriptions of current internal architecture.

### AI & Machine Learning

Perceptrons and backpropagation · convolutional networks and AlexNet · recurrent models and LSTMs · attention and Transformers · BERT/GPT and scaling · instruction tuning and RLHF · GANs and diffusion · mixture-of-experts · embeddings and retrieval-augmented generation · GPU/CUDA and distributed training · quantization, LoRA/QLoRA, inference optimization, speculative decoding · multimodal models, agents, and alignment.

### Data Engineering

GFS and MapReduce · Hadoop/HDFS · Spark · Kafka and Flink · batch/stream processing · ETL/ELT · warehouses and lakes · Iceberg/Delta/Hudi · Parquet and columnar layouts · query engines · orchestration · quality, lineage, and governance.

### Cloud & Infrastructure

Virtual machines · Borg and cluster schedulers · Docker and Kubernetes · cloud primitives · distributed storage · CDN and edge · infrastructure as code · serverless · service meshes · software-defined networking · cloud security · automation and FinOps.

### Security & Reliability

Injection and browser attacks · SSRF and identity failures · API and supply-chain security · secrets · container security · Zero Trust · secure development · SRE and error budgets · incident command · chaos engineering · disaster recovery · postmortems.

### Engineering Failures

Outages · data loss · failed migrations · breaches · overload cascades · bad abstractions · over-decomposition · premature optimization · rewrites · lock-in · technical debt. Case studies will distinguish timeline/root-cause facts in source documents from lessons inferred afterward.

### Foundational Research Papers

The timeline links a starter set of original papers and technical documents. Each chapter will expand the bibliography with primary sources, publication dates, and follow-on work.

## Reading sequence

1. Use the timeline to form a map; do not attempt to memorize every milestone.
2. Pick a constraint (latency, coordination, storage, throughput, cost, or operability).
3. Read one original source and one operational account from a company that deployed the idea.
4. Draw the data path and at least one failure path.
5. Write the journal entry: learned, surprised, designed differently.

## Case-study template

1. Historical context and prior approaches
2. Original practical problem and scale
3. Binding technical bottleneck
4. Competing approaches and why they fell short
5. Breakthrough, authorship, architecture, and algorithm
6. Trade-offs, failure modes, and limitations
7. Adoption and industry consequences
8. Lessons, including where the design is a poor fit
9. Primary sources and further reading

For selected chapters, the opening will present the constraints before the historical solution so the reader can attempt a design first.
