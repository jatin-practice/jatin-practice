<h1 align="center">Jatin Kumar Rout</h1>

<p align="center">
<strong>Distributed Systems Architect</strong>
<br/>
18 Years Building Production Systems at Scale
<br/>
Bangalore, India — Open to Fully Remote Roles
</p>

<p align="center">
<a href="https://www.linkedin.com/in/jatinkumarrout">
<img src="https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin"/>
</a>
<a href="mailto:jatin.practice@gmail.com">
<img src="https://img.shields.io/badge/Email-Contact-red?style=flat&logo=gmail"/>
</a>
<img src="https://img.shields.io/badge/Remote-Available%20Now-green?style=flat"/>
<img src="https://img.shields.io/badge/Experience-18%20Years-orange?style=flat"/>
</p>

---

## What I Build

I build systems that work at scale — not just systems
that work. The difference matters when you have
millions of devices, terabytes of data, and
operations teams who cannot afford downtime.
```
1M+ network devices managed
TB scale data serving
100x throughput improvement
99.999% availability achieved
3.2M daily operations
Zero downtime credential rotation at fleet scale
```

---

## Open Source Projects

### NetFleet — Distributed Network Device Platform

> Production grade platform for managing large scale
> network device fleets at any scale

Built on real production experience managing 1M+
network devices across multiple regions and segments.
Five component distributed pipeline. Six vendor support
— Cisco IOS, Huawei VRP, Juniper JunOS, BDCOM,
ZTE ZXROS, UTStarcom. Three deployment profiles
from Docker Compose to full Kubernetes cluster.

Includes security module for zero downtime credential
rotation at fleet scale — zero lockout guarantee,
MAC and Serial based device identity, two phase
commit pattern, RBAC with segment wise access control.
```
Key design decisions:
    ThreadPool over AsyncIO
    — network device latency is unpredictable
    — one slow device in AsyncIO blocks hundreds

    Region basis delta validation
    — global threshold misses partial failures
    — region basis catches silent data loss

    MongoDB as independent microservice
    — separated from postprocessor for clean scaling
    — aggregator pattern with cache timeout safety net

    Pluggable transport — Redis or Kafka
    — one env variable switches deployment profile
    — business logic never changes
```

**Stack:** Python · FastAPI · Redis · Kafka · MongoDB
· Netmiko · TextFSM · Docker · Kubernetes

[![NetFleet](https://img.shields.io/badge/View-NetFleet-blue?style=flat&logo=github)](https://github.com/jatin-practice/netfleet)

---

### DataAccess — Unified Data Access Layer

> TB scale data access with zero schema binding,
> two layer cache and multi interface API

Built on real production experience serving TB scale
data to 50+ microservice clients at 99.999% availability.
Unified REST, GraphQL and gRPC interfaces over any
database. Pandas DataFrames in memory per pod.
Redis Cluster as shared persistent cache with
Pickle serialization. Zero schema binding for REST —
DB schema changes require zero code changes.
Virtual entities merge data from multiple databases
in a single API call.
```
Key design decisions:
    Pickle over JSON for DataFrame serialization
    — binary format, faster, smaller, type preserving
    — purpose built for DataFrame round trips

    Lazy loading at startup
    — nothing preloaded, service starts in seconds
    — entity loaded only when first requested

    Mutex on first load per entity
    — prevents cache stampede on cold start
    — only one request hits DB, others wait

    WAL before DB commit
    — no untracked writes ever
    — crash safe change tracking
    — dead letter queue for failed events

    Eventual consistency by design
    — acceptable for read heavy analytical workloads
    — must-revalidate header for strong consistency needs
```

**Stack:** Python · FastAPI · Pandas · Redis Cluster
· Kafka · SQL Server · PostgreSQL · Vertica
· Docker · Kubernetes

[![DataAccess](https://img.shields.io/badge/View-DataAccess-blue?style=flat&logo=github)](https://github.com/jatin-practice/dataaccess)

---

## Production Track Record

| Via | Role | Scale | Impact |
|---|---|---|---|
| Andela — Remote US | Senior Backend Engineer | TB scale cache | 99.999% availability |
| Direct | Senior Tech Lead / Architect | Analytics platform | 100x throughput |
| Direct | Sole Architect | 1M+ IoT devices | 3.2M daily ops |

---

## Technical Philosophy

**On choosing tools:**
The right tool is the one that fits the problem —
not the newest or most popular. ThreadPool over
AsyncIO when device latency is unpredictable.
Redis over Kafka when eventual consistency is
acceptable and operational simplicity matters.
Truncate and replace over row by row update
when atomicity matters more than incremental cost.

**On failure handling:**
Design for failure first. Every system fails.
The question is whether it fails gracefully or
catastrophically. Circuit breakers, retry budgets,
dead letter queues, cache timeouts — these are
not optional extras. They are what makes a system
production grade.

**On scale:**
Scale is not just about handling more requests.
It is about maintaining correctness, observability
and operability as load increases. A system that
works at 1000 devices but breaks at 100000 was
never really designed for production.

**On documentation:**
Code without context is a liability. The why matters
as much as the what. Every architectural decision
has a reason. Document it before you forget.

---

## Core Stack
```python
expertise = {
    "languages":   ["Python", "SQL", "Shell"],
    "backend":     ["Django", "FastAPI", "gRPC",
                    "GraphQL", "REST"],
    "distributed": ["Kafka", "Redis Cluster",
                    "Saga Pattern", "CDC", "WAL"],
    "databases":   ["MongoDB", "PostgreSQL",
                    "Redis", "Cassandra",
                    "SQL Server", "Vertica"],
    "data":        ["Pandas", "Spark", "PySpark",
                    "Hadoop"],
    "infra":       ["Docker", "Kubernetes",
                    "AWS", "Prometheus", "Grafana"],
    "protocols":   ["SNMP", "SSH", "Telnet",
                    "Netconf", "gRPC"],
    "currently":   ["LLM Applications", "RAG",
                    "Vector Databases"]
}
```

---

## Currently Exploring

Building toward LLM application engineering —
the intersection of my distributed systems background
with AI application layer. Strong backend and systems
knowledge maps directly to:
```
LLM API integration and optimization
RAG pipeline architecture
Vector database design
Async LLM call management
Rate limiting and cost optimization at scale
Production deployment of AI systems
```

The hardest problems in AI are not the models.
They are the systems that make models useful
at scale. That is where I am headed.

---

## Let us Connect

Open to fully remote Senior and Staff Backend
Engineer roles. Immediate availability.

Particularly interested in:
- Distributed systems at scale
- Platform and infrastructure engineering
- LLM application development
- Network automation and IoT platforms

<p align="center">
<a href="https://linkedin.com/in/python-jatinrout">LinkedIn</a>
·
<a href="mailto:jatin.practice@gmail.com">Email</a>
·
<a href="https://github.com/jatin-practice/netfleet">NetFleet</a>
·
<a href="https://github.com/jatin-practice/dataaccess">DataAccess</a>
</p>

---

<p align="center">
<em>Building systems that work at scale.<br/>
Not just systems that work.</em>
</p>
