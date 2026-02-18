# 🗄️ Windows Server Failover Cluster Deployment Lab

---

## 🧠 Objective

Design and deploy a highly available Windows Server 2016 failover cluster using shared iSCSI storage to simulate enterprise-level redundancy and fault tolerance.

---

## 🛠️ Technologies Used

- Windows Server 2016
- Failover Clustering
- iSCSI Target Server
- iSCSI Initiator
- RAID-5 Storage
- Hyper-V Virtual Machines
- Active Directory Domain Services
- Disk Management

---

## 🏗️ Environment Overview

| Role | Server Name | Purpose |
|------|------------|----------|
| Domain Controller | RWDC31 | Domain Services |
| Storage Server | Storage31 | iSCSI Target Server |
| Cluster Node 1 | Server31-A | Failover Cluster Node |
| Cluster Node 2 | Server31-B | Failover Cluster Node |

**Cluster Name:** `Cluster31`  
**Shared Storage:**  
- 2GB Quorum Disk  
- 8GB Data Disk  

---

# ⚙️ Project Implementation

---

## 1️⃣ Configured iSCSI Target Server

- Installed iSCSI Target Server role on Storage31  
- Created RAID-backed virtual disks:
  - 2GB QuorumDrive  
  - 8GB DataDrive31  
- Configured iSCSI target access for:
  - Server31-A  
  - Server31-B  
- Restricted access via IP-based initiator configuration  

---

## 2️⃣ Configured iSCSI Initiators (Cluster Nodes)

- Connected Server31-A and Server31-B to shared storage  
- Enabled Microsoft iSCSI service  
- Brought shared disks online  
- Initialized and formatted disks:
  - QuorumDisk  
  - DataDisk  

---

## 3️⃣ Installed Failover Clustering Feature

- Installed Failover Clustering on both cluster nodes  
- Verified feature installation via Server Manager  

---

## 4️⃣ Validated Cluster Configuration

- Ran **Validate Configuration Wizard**
- Tested:
  - Storage
  - Network
  - System configuration
- Confirmed all validation tests passed  

---

## 5️⃣ Created Failover Cluster

- Created new cluster: `Cluster31`
- Assigned static cluster IP address
- Added both nodes
- Added eligible shared storage
- Verified cluster disks under Storage → Disks  

---

# 🔎 Validation & Testing

- Confirmed both nodes visible in Failover Cluster Manager  
- Verified quorum disk assigned  
- Confirmed shared storage accessible across both nodes  
- Observed proper active-passive configuration  

---

# 🔐 Skills Demonstrated

- High Availability Infrastructure Design  
- Windows Failover Clustering  
- Shared Storage Configuration (iSCSI)  
- RAID-backed Storage Management  
- Enterprise Redundancy Implementation  
- Cluster Validation & Troubleshooting  

---

# 📷 Screenshots

### iSCSI Virtual Disks
![iSCSI Disks](https://i.imgur.com/xAZIEQv.png)

---

### iSCSI Initiator Configuration
![iSCSI Initiator](https://i.imgur.com/1rV2wgB.png)

---

### Failover Clustering Feature Installation
![Feature Installation](https://i.imgur.com/g6DBGLP.png)

---

### Cluster Validation Results
![Validation Results](https://i.imgur.com/JB9rDLR.png)

---

### Failover Cluster Manager – Storage View
![Cluster Manager](https://i.imgur.com/4yx1xQm.png)

---

# 🚀 Project Outcome

Successfully deployed a two-node Windows Server failover cluster using shared iSCSI storage, simulating enterprise-level high availability infrastructure with quorum configuration and storage validation.
