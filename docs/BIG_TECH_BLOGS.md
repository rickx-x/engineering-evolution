# Big Tech engineering blog directory

Official publications are valuable first-party records, but they are selective: posts are written to explain chosen systems and lessons, not to expose every internal detail. Treat each post as a dated engineering account; validate technical claims against the cited paper, docs, or incident report when available.

## Curated company directory

| Company | Official publication | Strongest areas | Recommended starting points and why |
|---|---|---|---|
| Google | [Google Research](https://research.google/pubs/) · [Google Cloud Blog](https://cloud.google.com/blog/) | Search, storage, distributed data, ML, infrastructure | [GFS (2003)](https://research.google/pubs/the-google-file-system/) and [MapReduce (2004)](https://research.google/pubs/mapreduce-simplified-data-processing-on-large-clusters/): foundational papers that expose workload assumptions and system design. Then [Borg (EuroSys 2015)](https://research.google/pubs/large-scale-cluster-management-at-google-with-borg/). |
| Amazon | [AWS Architecture Blog](https://aws.amazon.com/blogs/architecture/) · [Builders' Library](https://aws.amazon.com/builders-library/) | Reliability, distributed services, cloud primitives, operational practice | [Timeouts, retries, and backoff with jitter](https://aws.amazon.com/builders-library/timeouts-retries-and-backoff-with-jitter/): shows how local retry policy can amplify an outage. Pair with [Dynamo (2007)](https://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf) for deliberate availability/consistency trade-offs. |
| Meta | [Engineering at Meta](https://engineering.fb.com/) | Social graph, storage, ranking, infrastructure, mobile, AI | [TAO: Facebook's distributed data store for the social graph](https://engineering.fb.com/2013/06/25/core-infra/tao-the-power-of-the-graph/): a concrete read-optimized graph-serving design. Follow with [MySQL at Facebook](https://engineering.fb.com/2014/03/20/core-infra/mysql-at-facebook/). |
| Netflix | [Netflix TechBlog](https://netflixtechblog.com/) | Streaming, cloud operations, resilience, personalization, data | [The Netflix Simian Army (2011)](https://netflixtechblog.com/the-netflix-simian-army-16e57fbab116): tests fault tolerance through controlled failure. Pair with [Netflix's migration to the cloud](https://about.netflix.com/en/news/four-reasons-we-choose-aws) for the strategic context. |
| Uber | [Uber Engineering](https://www.uber.com/blog/engineering/) | Geospatial systems, marketplace, streaming, ML, reliability | [The Uber Engineering Blog](https://www.uber.com/blog/engineering/) includes the H3 geospatial indexing system and marketplace infrastructure; read the H3 paper/docs alongside posts to distinguish index properties from product use. |
| LinkedIn | [LinkedIn Engineering](https://engineering.linkedin.com/) | Kafka, stream processing, search, graph, data infrastructure | [How we're improving and advancing Kafka at LinkedIn (2015)](https://engineering.linkedin.com/apache-kafka/how-we_re-improving-and-advancing-kafka-linkedin): documents Kafka's operational growth from 1B messages/day in 2011 to 200B/day in 2013. |
| Microsoft | [Microsoft Engineering](https://devblogs.microsoft.com/engineering-at-microsoft/) · [Azure Architecture Blog](https://azure.microsoft.com/en-us/blog/topics/architecture/) | Cloud platform, developer tools, security, databases, AI systems | Use the engineering blog for org-scale platform practice and Azure Architecture posts for service designs; pair product accounts with primary research papers where possible. |
| Apple | [Apple Machine Learning Research](https://machinelearning.apple.com/) · [Apple Security Research](https://security.apple.com/blog/) | On-device ML, privacy, silicon-aware inference, security | Start with papers and technical posts on on-device models and private ML; the journal is research-led rather than a general infrastructure diary. |
| Cloudflare | [Cloudflare Blog](https://blog.cloudflare.com/) | Internet routing, CDN, edge compute, DDoS, DNS, security | [How we built Pingora](https://blog.cloudflare.com/how-we-built-pingora-the-proxy-that-connects-cloudflare-to-the-internet/): a production proxy rewrite framed around memory safety and resource efficiency. Follow with Cloudflare outage postmortems, which often include concrete causal chains. |
| Stripe | [Stripe Engineering](https://stripe.com/blog/engineering) · [Stripe Blog](https://stripe.com/blog) | Payments, API design, idempotency, ledgers, reliability | [Designing robust and predictable APIs with idempotency](https://stripe.com/blog/idempotency): a payment-domain example of making retries safe under uncertain network outcomes. |
| Airbnb | [Airbnb Engineering & Data Science](https://airbnb.tech/) | Search, experimentation, data, ML, marketplace | Start with [Chronon](https://github.com/airbnb/chronon), an open-source feature platform, and Airbnb's engineering articles on experimentation/data infrastructure; follow links to the original technical design. |
| Spotify | [Spotify Engineering](https://engineering.atspotify.com/) | Personalization, data, experimentation, developer platform | [Backstage](https://backstage.io/blog/): an internal developer portal opened to the industry. Read the original Spotify post explaining the problem of scattered service ownership and tooling. |
| Discord | [Discord Blog](https://discord.com/blog) | Real-time messaging, storage, voice, performance | [How Discord stores billions of messages](https://discord.com/blog/how-discord-stores-billions-of-messages): useful as a dated case study of datastore scaling and migration trade-offs. |
| Shopify | [Shopify Engineering](https://shopify.engineering/) | Commerce, Ruby/Rails, storage, reliability, developer experience | Start with [Deconstructing the Monolith](https://shopify.engineering/deconstructing-monolith-designing-software-maximizes-developer-productivity): a counterweight to reflexive microservice adoption and a lesson in modularity. |
| Pinterest | [Pinterest Engineering](https://medium.com/@Pinterest_Engineering) | Search/discovery, recommendation, data, reliability | Read the engineering archive by topic (search, recommendation, MySQL, cache) and trace claims to dated posts; its historical Medium archive has moved over time. |
| Dropbox | [Dropbox Tech](https://dropbox.tech/) | Storage, synchronization, networking, client engineering | [Magic Pocket](https://dropbox.tech/infrastructure/magic-pocket-infrastructure): a first-party account of Dropbox's custom storage infrastructure and the economic/operational reasons for building it. |
| Reddit | [Reddit Engineering](https://redditinc.com/blog/engineering) | High-volume community product, ranking, platform operations | The public engineering archive is less continuous than some peers. Search by concrete systems and favor posts with architecture detail, publication dates, and source links. |

## Suggested reading order by question

| If you want to understand… | Read first | Then compare with |
|---|---|---|
| Distributed storage under different consistency goals | Google GFS / Bigtable | Amazon Dynamo, Meta TAO, Dropbox Magic Pocket |
| Streaming data and event logs | LinkedIn Kafka accounts | Uber streaming and real-time marketplace posts |
| Resilience under failure | Netflix Simian Army | AWS Builders' Library retries, Cloudflare postmortems |
| Service boundaries and team productivity | Shopify monolith design | Spotify Backstage, Netflix service platform accounts |
| Internet edge and networking | Cloudflare engineering posts | Google network papers and AWS global infrastructure materials |
| Product correctness with retries | Stripe idempotency | AWS idempotent APIs and retry guidance |
| AI systems in production | Google Research / Apple ML Research | Meta Engineering AI posts and Netflix personalization posts |

## Reading method

For each post, record: (1) publication date and system scope, (2) workload and bottleneck, (3) what the authors state they chose, (4) failure mode or operational cost, (5) which parts generalize and which depend on company scale. See the [journal template](../journal/README.md).

## Maintenance note

Links can move as companies reorganize their publishing platforms. The directory favors stable official landing pages, papers, and canonical posts where known. Recheck article URLs and publication dates when extending a chapter; do not treat this starter directory as a complete feed.
