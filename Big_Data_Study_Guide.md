# Big Data, Hadoop, and Spark Study Guide

---

## Part 1: Short Answer Quiz

Answer the following questions in 2-3 sentences each.

1. **What are the "Five V's" used to classify data as Big Data?**

2. **Describe the two core components of the original Hadoop framework.**

3. **What is the primary role of a Big Data Engineer in an organization?**

4. **Explain the concept of data replication in the Hadoop Distributed File System (HDFS) and its default setting.**

5. **What is Apache Spark, and how does its approach to data processing differ from Hadoop MapReduce?**

6. **Briefly describe YARN and its main components within the Hadoop ecosystem.**

7. **What is the fundamental difference between Hive and Pig?**

8. **What is a NoSQL database, and what are its key features?**

9. **Explain the purpose of Scoop in the Hadoop ecosystem.**

10. **What is a Recommender System, and what is the core principle behind Collaborative Filtering?**

---

## Part 2: Answer Key

1. **Five V's:** Volume (amount of data), Velocity (speed of data generation), Variety (different data formats), Veracity (quality/trustworthiness), Value (usefulness for business).

2. **Hadoop Core Components:**

   * **HDFS:** Storage layer, splits large files into blocks distributed across nodes.
   * **MapReduce:** Processing engine, splits tasks into map (processing) and reduce (aggregating) phases.

3. **Big Data Engineer Role:** Develops, maintains, and tests data infrastructure, designs ETL pipelines, builds scalable architectures, collaborates with architects, analysts, and data scientists.

4. **Data Replication in HDFS:** Copies data blocks across multiple nodes for fault tolerance. Default replication factor: **3**.

5. **Apache Spark:** In-memory computing framework, faster than MapReduce because it avoids disk I/O and supports batch & real-time processing.

6. **YARN Components:**

   * Resource Manager (allocates resources)
   * Node Managers (monitor resources on nodes)
   * Application Master (manages resources for each app)
   * Containers (CPU/RAM allocation for tasks)

7. **Hive vs Pig:** Hive uses SQL-like declarative HQL for structured data; Pig uses procedural Pig Latin for complex transformations on structured, semi-structured, or unstructured data.

8. **NoSQL Database:** Non-relational, handles unstructured/semi-structured data, dynamic schema, horizontal scalability, key-value/document/column-based data models.

9. **Scoop:** Transfers bulk data between Hadoop and relational databases; performs import/export tasks efficiently using YARN.

10. **Recommender System & Collaborative Filtering:** Predicts user preferences based on similar users (user-based) or items (item-based).

---

## Part 3: Essay Questions

1. **Hadoop vs Spark Architectures & Use Cases:**

   * Hadoop: Disk-based, batch processing, uses HDFS + MapReduce.
   * Spark: In-memory, batch & real-time processing, faster.
   * Evolution: Spark evolved to reduce MapReduce disk I/O overhead.
   * Choice: Use Hadoop for large-scale batch jobs and Spark for real-time analytics or faster processing.

2. **HDFS Architecture & Operations:**

   * Components: NameNode, DataNodes, Secondary NameNode, replication, rack awareness.
   * **Data Read:** Client → NameNode (block locations) → DataNodes (fetch blocks).
   * **Data Write:** Client → NameNode (allocate blocks) → DataNodes (write data + replicate) → Acknowledgement.

3. **Big Data Engineer Profile:**

   * Responsibilities: Develop infrastructure, ETL, data pipelines, optimize systems.
   * Skills: Hadoop, Spark, Python/Java, SQL/NoSQL, ETL, data modeling, cloud computing.
   * Certifications: Cloudera, Hortonworks, AWS Big Data Specialty, Databricks.

4. **NoSQL Database Patterns:**

   * **Key-Value:** Fast lookups (Redis, DynamoDB).
   * **Column Store:** Column-based storage, analytical queries (HBase, Cassandra).
   * **Document:** Semi-structured JSON/BSON documents (MongoDB, CouchDB).
   * **Graph:** Nodes & edges, relationships & traversal (Neo4j, FlockDB).

5. **Big Data Analytics Lifecycle:**

   * Steps: Data gathering → storage → processing → analysis → decision-making.
   * Types: Descriptive, Predictive, Prescriptive, Diagnostic.
   * Application in e-commerce: Analyze customer behavior, predict preferences, optimize recommendations, improve sales.

---

## Part 4: Glossary of Key Terms

| Term                           | Definition                                                                          |
| ------------------------------ | ----------------------------------------------------------------------------------- |
| ACID Compliance                | Atomicity, Consistency, Isolation, Durability; full compliance not always in NoSQL. |
| Agility                        | Ability to rapidly develop/adapt software; supported by NoSQL flexible schema.      |
| Apache Spark                   | Open-source in-memory computing engine for batch and real-time data.                |
| Application Master (AM)        | Temporary daemon in YARN managing resources for each application.                   |
| Atom                           | Pig data type representing a single simple value.                                   |
| Bag                            | Pig data type: unordered collection of tuples.                                      |
| Big Data                       | Massive data that traditional systems can't handle; defined by 5 V's.               |
| Big Data Architect             | Designs large-scale big data systems and Hadoop applications.                       |
| Big Data Engineer              | Develops, maintains, tests, and evaluates big data infrastructure.                  |
| Cassandra                      | Column-family NoSQL database with fault tolerance via replication.                  |
| Collaborative Filtering        | Recommender system method using similar user/item preferences.                      |
| Column Store Database          | Stores data by columns; efficient for analytical queries.                           |
| Commodity Hardware             | Inexpensive standard computers forming Hadoop clusters.                             |
| Container                      | YARN resource allocation unit for CPU, RAM, bandwidth.                              |
| Content-based Filtering        | Recommender system method suggesting items similar to those previously liked.       |
| D-Stream (Discretized Stream)  | Spark Streaming abstraction representing continuous data stream.                    |
| Data Node                      | HDFS worker node storing data blocks.                                               |
| Document Database              | Stores flexible documents (JSON/BSON); MongoDB, CouchDB.                            |
| ETL (Extract, Transform, Load) | Process of ingesting, transforming, and storing data.                               |
| Federation (Hadoop)            | Multiple independent NameNodes sharing DataNodes for scalability.                   |
| Graph Database                 | Represents data as nodes & edges for complex relationships; Neo4j.                  |
| Hadoop                         | Framework for distributed storage (HDFS) and processing (MapReduce/YARN).           |
| Hadoop Common                  | Core utilities and libraries supporting Hadoop modules.                             |
| HDFS                           | Hadoop's distributed storage layer with block replication.                          |
| HMaster                        | HBase master process managing regions and DDL operations.                           |
| HQL (Hive Query Language)      | SQL-like language used in Hive to query HDFS data.                                  |
| HBase                          | Column-oriented NoSQL database on top of HDFS.                                      |
| Hive                           | Data warehouse on Hadoop with SQL-like queries.                                     |
| High Availability (Hadoop)     | Active-standby NameNode configuration to prevent downtime.                          |
| Key-Value Store Database       | Stores data as key-value pairs (Redis, DynamoDB).                                   |
| Map (Pig Data Type)            | Collection of key-value pairs in Pig.                                               |
| MapReduce                      | Hadoop processing model: Map phase + Reduce phase.                                  |
| Metastore                      | Hive component storing metadata about tables and databases.                         |
| MongoDB                        | Document-oriented NoSQL database storing JSON-like BSON data.                       |
| NameNode                       | HDFS master server managing namespace & metadata.                                   |
| NoSQL                          | Non-relational database handling unstructured/semi-structured data.                 |
| Node Manager                   | YARN process on each node managing resources and containers.                        |
| Pig                            | High-level data processing platform for Hadoop using Pig Latin.                     |
| Pig Latin                      | Procedural data-flow language used in Pig.                                          |
| RDD                            | Spark's Resilient Distributed Dataset; immutable & parallel.                        |
| Rack Awareness                 | Ensures HDFS replicas stored across different racks.                                |
| Recommender System             | Predicts user preferences; used in e-commerce/streaming.                            |
| Region Server                  | HBase worker managing table regions and handling read/write.                        |
| Replication                    | HDFS copies data blocks to multiple nodes; default factor 3.                        |
| Resource Manager (RM)          | YARN master managing cluster-wide resources.                                        |
| Scoop                          | Transfers data between Hadoop and external RDBMS.                                   |
| Social Media Mining            | Extracting insights from social media data.                                         |
| Social Network Graph           | Graph representation of users and relationships.                                    |
| Tuple                          | Pig data type: ordered set of fields.                                               |
| YARN                           | Hadoop 2.0 resource manager & job scheduler.                                        |
| Zookeeper                      | Coordination service for distributed systems; used in HBase.                        |

---

This Markdown file preserves **all your content**, is easy to read, and can be converted to PDF with proper formatting.
