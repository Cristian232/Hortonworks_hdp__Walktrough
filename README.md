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

---

### Step 2: Import OVA into VirtualBox
1. Open VirtualBox application
2. Click **File** > **Import Appliance**
3. Select the downloaded `HDP_3.0.1_virtualbox_181205.ova` file

<img width="1972" height="1737" alt="image" src="https://github.com/user-attachments/assets/1b2d00d4-cd9d-4259-9b43-76c78b0ba4db" />

4. Review default settings (8 GB RAM, 2 CPUs recommended)
5. Set the Machine Base Folder to a folder that has 100 GB free 

<img width="1602" height="1182" alt="image" src="https://github.com/user-attachments/assets/58d48d41-f346-4b78-ab6c-526c3e251dc8" />

6. Click **Import** and wait for the process to complete (approximately 10-15 minutes)

<img width="397" height="247" alt="image" src="https://github.com/user-attachments/assets/ebcc5635-8510-41e8-9b25-404755d98e76" />

7. Finish

<img width="2549" height="1593" alt="image" src="https://github.com/user-attachments/assets/3f3e405a-4bc5-4fdb-adf6-19fd69d6fbe8" />


---



### Step 3: Start the Virtual Machine
1. Select the HDP Sandbox VM
2. Click **Start**
3. Wait for the VM to boot (first boot takes 5-10 minutes)

<img width="2545" height="1661" alt="image" src="https://github.com/user-attachments/assets/86671625-31cf-42fa-b238-32688a960e00" />


4. After succesfull start will appear the following:

<img width="975" height="701" alt="image" src="https://github.com/user-attachments/assets/3aaddc2d-d4ba-4fe9-8976-5f659ea9e6c3" />

---

### Step 4: Access HortonWorks Sandbox Web Interface
1. Open web browser on host machine
2. Navigate to: `http://localhost:1080`


<img width="2552" height="1808" alt="image" src="https://github.com/user-attachments/assets/c0794a0f-4b7d-4819-b30c-65c04dc172ac" />


3. Recommended -> Access Quick links (right side)

<img width="2541" height="1687" alt="image" src="https://github.com/user-attachments/assets/598fe54a-b811-4274-9303-bbb928329ee5" />


---


### Step 5: Access Ambari Web Interface
1. Open web browser on host machine
2. Navigate to: `http://localhost:8080` or from `http://localhost:1080` Advanced HDP Quick Links -> Ambari `Go to UI`

<img width="2145" height="1028" alt="image" src="https://github.com/user-attachments/assets/64d1ced9-f948-4910-8876-5c4449862f12" />

3. Login with Ambari credentials:
   - Username: `raj_ops`
   - Password: `raj_ops`

4. Verify all services are running (green status indicators)

<img width="2522" height="2061" alt="image" src="https://github.com/user-attachments/assets/3273b62c-6bb8-4f10-bdbe-eb34e47613a5" />

Likely a legacy UI, need to scroll down for the next screen

<img width="2543" height="1781" alt="image" src="https://github.com/user-attachments/assets/6dcaf68a-82bf-4f7e-916b-708233c877fb" />

---

### Step 6: Access ssh 
**SSH Connection Test:**
```powershell
ssh root@localhost -p 2222
# Password: hadoop (or your changed password)
````
Will be required to change pass

<img width="2758" height="594" alt="image" src="https://github.com/user-attachments/assets/15131570-9c6d-46c1-bfa1-5f1c41c48460" />

<img width="2755" height="105" alt="image" src="https://github.com/user-attachments/assets/55dd85bf-b25e-4e67-a736-782b9638843c" />


Common commands

# Check HDFS status (run as hdfs user)
sudo -u hdfs hdfs dfsadmin -report

<img width="2756" height="1796" alt="image" src="https://github.com/user-attachments/assets/63e05fec-80e8-43fa-92f0-48c3cf77af9c" />

# List HDFS root directory
sudo -u hdfs hdfs dfs -ls /

<img width="2757" height="728" alt="image" src="https://github.com/user-attachments/assets/a02866ba-c2fd-4862-9a17-f4e2adb6454c" />

````
# Create directory in HDFS
sudo -u hdfs hdfs dfs -mkdir /user/yourname

# Upload file to HDFS
sudo -u hdfs hdfs dfs -put localfile.txt /user/yourname/
````
