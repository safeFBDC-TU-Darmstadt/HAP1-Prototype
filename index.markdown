---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

# Welcome to safeFBDC-HAP1-Prototype

This is an introduction paragraph...

## Data Management Lab

The finished and published work of the Data Management Lab is centered around two main topics: verifiable and secure data sharing and secure and privacy-preserving federated ML.

### Verifiable and Secure Data Sharing

This is an introductory paragraph for data sharing with blockchains.

#### Lock Manager for Blockchains

New systems for decentralized data sharing are becoming increasingly important. Blockchains are often used for the underlying storage layer to implement such systems. This is because a blockchain maintains an immutable transaction log that enables trustworthy audits of past transactions when needed. However, blockchains come with two major challenges that must be overcome for this idea to become a reality:

1. Scalability and performance issues
2. The lack of common abstractions offered by a relational DBMS, such as an SQL query interface and sophisticated transaction processing with well-defined consistency levels.

A recently completed bachelor thesis focuses on the second aspect. It proposes a new locking-based protocol to provide ACID-compliant transaction processing on multiple shared blockchains. As a core, a lock manager has been implemented to organize locks of multiple transactions from different parties on the shared data.

> Thesis Title: Verifiable Lock Manager using Intel SGX\
> Author: Henry Helm\
> Repository containing source code: Link

#### ACID-V

We developed a new reference architecture for trusted and secure data sharing that enables secure sharing and collaborative processing of data across multiple financial institutions. A paper on these results has been accepted.

In this paper, we propose a new approach to providing verifiability for shared data systems. The main idea is to extend the ACID properties used by classical DBMSs with a new verifiability component that leads to ACID-V properties. More specifically, similarly to the other components of ACID, such as the well-known isolation property, we propose to specify verifiability guarantees declaratively, using different levels of verification (i.e., strict or more loose). Moreover, we believe that integrating verification with the ACID properties is not only a natural fit, providing well-defined guarantees to applications, but also enables a new class of shared DBMSs. These new DBMSs decide based on the level of verification which optimizations and concrete execution strategies are best suited to satisfy the desired guarantees.

> Publication Title: ACID-V: Towards a New Class of DBMSs for Data Sharing\
> Authors: Muhammad El-Hindi, Zheguang Zhao, Carsten Binnig\
> Publication Link: <https://doi.org/10.1007/978-3-030-93663-1_5>\
> Repository containing source code: Link

### Secure and Privacy-Preserving Federated Machine Learning

Federated learning has emerged as a promising paradigm for privacy-preserving machine learning, where multiple parties jointly train a machine learning model on their private data, i.e., without sharing the data with the other parties. Recently, however, several vulnerabilities have been discovered that can lead to compromised global model integrity and privacy.

#### Client-side Validation for Efficient Model Poisoning Detection in Federated Learning

Model poisoning attacks are among the most serious threats to model integrity in federated learning. In such an attack, an attacker attempts to corrupt the global model by altering parts of the training process. Several defenses to make federated learning resilient to these attacks have already been introduced.

However, in some scenarios, such as heterogeneous data, the state of the art defense mechanisms are less effective. Therefore, a recently completed master thesis proposes a general framework for secure federated learning. This new framework applies client-side training validation to reliably detect model poisoning attacks. Various randomized validation algorithms are proposed and analyzed to find a trade-off between efficiency, scalability, and security guarantees. The evaluation shows that the framework is able to robustly detect model poisoning, even for lowest level manipulations near the numerical limit, while incurring only a small overhead over training time.

> Thesis Title: Client-side Validation for Efficient Model Poisoning Detection in Federated Learning.\
> Author: Benedikt Völker\
> Repository containing source code: Link

## Software Technology Group

## AI & ML Lab
