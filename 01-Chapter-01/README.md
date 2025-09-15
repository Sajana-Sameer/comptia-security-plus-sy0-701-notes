# Chapter 01 Notes
# Chapter 1 — Mastering Security Basics (CompTIA Security+ SY0-701)

## Overview
This chapter lays the foundation for security: the **CIA Triad** (Confidentiality, Integrity, Availability), **security controls**, logging & monitoring, redundancy, fault tolerance, and resilience. Everything here maps closely to exam objectives and real-world practice.

---

## 1. The CIA Triad
- **Confidentiality** — Ensure data is accessible only to authorized parties.  
- **Integrity** — Ensure data remains accurate and untampered.(unauthorized updation)  
- **Availability** — Ensure systems and data are available when needed.

---

## 2. Ensuring Confidentiality
**Main approaches:**
- **Encryption**
  - Encryption scrambles data to make it unreadable by unauthorized personnel.
    eg : Advanced Encyption Standard(AES) - encryption algorithms
- **Access Control**
  - **Identification** — Claim identity (username, ID).  
  - **Authentication (AuthN)** — Prove identity (passwords, MFA, biometrics).  
  - **Authorization (AuthZ)** — Grant access rights (RBAC, ACLs).  
  - **Least Privilege** — Users/services get minimum permissions required.  
  - **Separation of Duties** — Prevent one person from having conflicting control.

---

## 3. Ensuring Integrity
- **Hashing**
  - Hash is an alphanumeric string created by executing a hashing algorithms.
  - One-way functions to create fingerprints of data.  
  - **MD5** — outdated, collision-prone.  
  - **SHA-256/SHA-512** — recommended secure hash algorithms.(SHA - Secure Hash Algorithm)
- **Digital Signatures** — Verify integrity and origin.  
- **File Integrity Monitoring** — Tools like Tripwire detect unexpected changes.

---

## 4. Ensuring Availability
**Redundancy & Fault Tolerance**
- Redundancy adds duplication to critical systems and provides fault tolerance.
- A common goal of fault tolerance and redundancy techniques is to remove each single point of failure (SPOF).
- **Disk redundancy (RAID)**
  - **RAID 1 (Mirroring)** — duplicate data across two disks.  
  - **RAID 5 (Striping with parity)** — stripe data across ≥3 disks with parity, tolerates single disk failure.  
  - **RAID 10 (Mirroring + Striping)** — combine mirroring and striping for high performance and fault tolerance.

- **Server redundancy**
  - Clustering, virtualization, failover for continuous service.

- **Network redundancy**
  - Load balancing across multiple servers.  
  - NIC teaming/bonding for failover or throughput (active/passive or LACP).  
  - Redundant network paths and switches/routers.

- **Power redundancy**
  - UPS for short-term power.  
  - Backup generators for long outages.  
  - Dual power supplies on servers and PDUs.

**Scalability & Elasticity**
- Scalability means that you are able to increase the capacity of a system or service to meet new     demand.
- Horizontal scaling (scale out: add servers/nodes).  
- Vertical scaling (scale up: add CPU/memory to a single server).  
- Elasticity: automatic scale up/down in response to demand.

**Resiliency**
- Ability to continue operating or recover quickly after failure.  
- NIC teaming, clustering, automatic failover.  

**Patching**
- Regularly update software/hardware to fix bugs and security issues.

**Resource availability vs security constraints**
- Trade-offs: security measures (encryption, monitoring) may impact performance; balance is key.

---

## 5. Security Controls
**Risk** 
- the possibility or likelihood of a threat exploiting a vulnerability resulting in a loss.
  
**Threat**
- any circumstance or event that has the potential to compromise confidentiality, integrity, or availability.
  
**Vulnerability**
- weakness in the hardware, the software, the configuration, or even the users operating the system.
  
**security incident**
- an adverse event or series of events that can negatively affect the confidentiality, integrity, or availability of an organization’s information technology (IT) systems and data.
   
**Control Functions (Types)**
- describes the goal that the control is trying to achieve.
  
1. Preventive — Stop incidents (firewalls, MFA).  
2. Detective — Detect incidents (IDS/IPS, SIEM alerts).  
3. Corrective — Restore/remediate (backups, patching).  
4. Deterrent — Discourage attacks (warnings, visible cameras).  
5. Compensating — Alternative control when primary is unavailable.  
6. Directive — Policies and instructions (security policies, SOPs).

**Control Categories**
- Describes how a control works.
  
- Technical — Technology-based (firewalls, IAM, encryption).  
- Managerial — Governance (policies, risk assessments).  
- Operational — People/processes (training, incident response).  
- Physical — Guards, locks, surveillance.

---

## 6. Logging & Monitoring

**Log types**
1. **Windows logs** — Event Viewer: Application, System, Security.  
2. **Network logs** — Firewall, IDS/IPS, packet captures (tcpdump/Wireshark), router/switch syslogs.  
3. **Application logs** — Web/app server logs (Apache/Nginx, DB logs).

**Centralized logging & SIEM**
- Syslog (forward logs from devices to a central server).  
- SIEM: Splunk, ELK Stack, IBM QRadar, Microsoft Sentinel.  
- Benefits: faster detection, correlation, compliance, forensic analysis.

---

## 7. Practice Questions
1. Which control function is a firewall?  
   - A) Detective  
   - ✅ B) Preventive  
   - C) Corrective  
   - D) Deterrent

2. Which RAID level offers striping with distributed parity?  
   - A) RAID 0  
   - ✅ B) RAID 5  
   - C) RAID 1  
   - D) RAID 10

3. Which is NOT a main log type covered in this chapter?  
   - A) Windows logs  
   - B) Network logs  
   - ✅ C) Hardware logs  
   - D) Application logs

---

## 8. Notes & Reminders
- Authentication ≠ Authorization (AuthN vs AuthZ).  
- MD5 is outdated; use SHA-256+.  
- Resilience and redundancy are key for availability.  
- Centralized logging + SIEM is essential for enterprise environments.

---

## Next Steps
- Add diagrams in `01-Chapter-01/assets/` (CIA Triad).  
- Add more end-of-chapter practice questions.  
- Create a short **Cheat-Sheet** for Chapter 1 in `Cheat-Sheets/Chapter-01.md`.



