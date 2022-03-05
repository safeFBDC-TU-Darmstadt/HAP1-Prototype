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

In the context of SafeFDBC:

REScala’s reactive programming support could be helpful to develop complex UI based tooling (control centers, monitoring) for any of the developed solutions. Furthermore, REScala does allow flexible replacements of its schedulers, thus reusing the language surface (declarative dataflow definitions) for other purposes – specifically, for more data processing focused pipelines. Reusing REScala here would both allow us to profit from our internal experience, but also make it easier to integrate data processing, with interactive applications.

REScala’s support for convergent data types is still somewhat experimental, as we experiment with a language-integrated approach to design applications together with data types. In particular, this allows developers to separate application logic, reasoning about distributed consistency (causal consistency to be specific), and the message dissemination logic – while at the same time all pieces as flexible modules in the language runtime and can be adapted and optimized for the current use case if necessary. In particular, we have used this architecture to implement transparent encryption of data on untrusted intermediaries in about 15 lines of code. More generally, we believe this approach is well suited to implement all manners of coordination protocols (ranging from management of encrypted states, over consensus, to opportunistic optimizations) in a manner that only requires local reasoning from the developer, but can be executed completely decentralized. Specifically, in the context of SafeFDBC demonstrator this could be useful as a basis for the coordination between banks (i.e., the decisions which data may be used by what applications, etc), as the approach also naturally provides a complete history of all past decisions and the current state to all participants (if not specifically optimized away or hidden). See the preprint paper: http://www.st.informatik.tu-darmstadt.de/preprints/2021-12_preprint_ECOOP_EnCRDTs.pdf

We have solutions for “tierless” programming, i.e., programming a diverse range of devices and their communication as a single source program (where the different “tiers” such as client/server are no longer fundamental differences in the programming model). Of maybe particular interest to the safeFDBC project, includes programming of smart contracts as one of the tiers, where we then can automatically infer correctness criteria that the contract relies on from the specification of the off-contract program code. This enables to check these criteria dynamically, thus preventing attacks where the off-contract program has been replaced by one that does not adhere to the specified behaviors.



## AI & ML Lab
