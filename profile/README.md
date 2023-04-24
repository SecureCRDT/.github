SecureCRDT
=============

This GitHub organization contains all the resources needed to deploy and evaluate the performance of SecureCRDT, a system published in the paper "General-Purpose Secure Conflict-free Replicated Data Types."


### What is SecureCRDT?

Conflict-free replicated data types (CRDTs) are data structures used to obtain strong eventual consistency in distributed storage systems. However, like other storage and processing systems, CRDTs raise privacy concerns. Specifically, third-party providers that host CRDT replicas can access and learn the contents of the data stored in the replicas. Classical encryption schemes, such as symmetric encryption, can't resolve this issue as secure CRDT protocols require replica-side computation to propagate operations.

SecureCRDT is a solution to address this problem with secure multiparty computation (MPC). With our system, we show that CRDT replicas can update their state over encrypted data. More generally, this approach can be applied to lift general-purpose implementations of CRDTs into secure variants. Our experimental prototype is implemented in Java and each CRDT replica consists of three parties that process requests using the Sharemind protocols.
