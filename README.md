# Hortonworks HDP Sandbox VM Setup Walkthrough

**Keywords:** Hortonworks, HDP, Hadoop, Big Data, Virtual Machine, VirtualBox, Data Engineering, Tutorial, Apache Spark, Apache Hive, Apache HBase, HDFS, YARN, Ambari, Zeppelin

## Overview
This repository contains a complete walkthrough for setting up Hortonworks HDP (Hortonworks Data Platform) Sandbox version 3.0.1 in a virtual machine environment.

## What is Hortonworks HDP Sandbox 3.0.1?
Hortonworks HDP Sandbox 3.0.1 is a pre-configured virtual machine that provides a self-contained Hadoop ecosystem environment. It enables learning, development, and testing of big data applications without requiring a full production cluster setup. The sandbox includes the complete Hortonworks Data Platform stack with distributed computing, storage, and data processing frameworks.

## Use Case
This guide supports the Distributed Data Engineering course curriculum for Master's students in Data Science at the University of Bucharest, Faculty of Mathematics and Computer Science (Year II, Semester I).

## Technical Specifications
- **Platform:** Hortonworks Data Platform (HDP)
- **Version:** 3.0.1
- **Format:** VirtualBox OVA
- **Download Size:** 20 GB
- **Unpacked Size:** 90 GB (ensure sufficient disk space)
- **VM Download:** https://archive.cloudera.com/hwx-sandbox/hdp/hdp-3.0.1/HDP_3.0.1_virtualbox_181205.ova

## Included Technology Stack
- **Apache Ambari** - Cluster management and monitoring
- **Apache Hadoop (HDFS)** - Distributed file system
- **Apache YARN** - Resource management
- **Apache MapReduce** - Distributed data processing
- **Apache Hive** - SQL query engine for Hadoop
- **Apache HBase** - NoSQL database
- **Apache Spark** - Fast distributed computing engine
- **Apache Zeppelin** - Web-based notebook for data analytics
- **Apache Pig** - High-level data flow scripting
- **Apache Sqoop** - Data transfer between Hadoop and relational databases
- **Apache Oozie** - Workflow scheduler
- **Apache Kafka** - Distributed streaming platform
- **Apache Storm** - Real-time stream processing
- **Apache Flume** - Log aggregation
- **Apache Zookeeper** - Distributed coordination service
- **Apache Atlas** - Data governance and metadata management
- **Apache Ranger** - Security framework
- **Apache Knox** - REST API gateway

---


## Installation Steps

### Prerequisites
- VirtualBox 6.0 or higher installed on your system. I have 7.2.2 currently.
- Minimum 16 GB RAM available (8 GB allocated to VM)
- 100 GB free disk space (90 GB for unpacked VM + overhead)

### Step 1: Download the HDP Sandbox
1. Navigate to the Cloudera archive:  https://archive.cloudera.com/hwx-sandbox/hdp/hdp-3.0.1/HDP_3.0.1_virtualbox_181205.ova
2. Download the file: `HDP_3.0.1_virtualbox_181205.ova` (20 GB)
3. Verify the download completed successfully

<img width="2624" height="1616" alt="image" src="https://github.com/user-attachments/assets/84851ae6-5132-4009-b855-eb7239584e28" />


