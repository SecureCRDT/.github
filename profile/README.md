SecureCRDT
=============
<img src="https://img.shields.io/badge/status-research%20prototype-green.svg" />

This GitHub organization contains all the resources needed to deploy and evaluate the performance of SecureCRDT, a system published in the paper "General-Purpose Secure Conflict-free Replicated Data Types".


### What is SecureCRDT?

Conflict-free replicated data types (CRDTs) are data structures used to obtain strong eventual consistency in distributed storage systems. However, like other storage and processing systems, CRDTs raise privacy concerns. Specifically, third-party providers that host CRDT replicas can access and learn the contents of the data stored in the replicas. Classical encryption schemes, such as symmetric encryption, can't resolve this issue as secure CRDT protocols require replica-side computation to propagate operations.

SecureCRDT is a solution to address this problem with secure multiparty computation (MPC). With our system, we show that CRDT replicas can update their state over encrypted data. More generally, this approach can be applied to lift general-purpose implementations of CRDTs into secure variants. Our experimental prototype is implemented in Java and each CRDT replica consists of three parties that process requests using the Sharemind protocols.

### How to run SecureCRDT?

SecureCRDT has three main components that need to be installed:

- SMPC: A Java library that implements the Sharemind protocols.
- SecureCRDT: A CRDT replica that utilizes the SMPC library to store and process data with secret sharing and SMPC protocols.
- Benchmark: The benchmark and workload definitions to measure the performance of the SecureCRDT system.

Each of these components has a README file with instructions on how to install and deploy them.

### How to run the benchmark?

To run the benchmark, follow these steps:
1. Install the SMPC library in your system according to the project README
2. Install the SecureCRDT project according to its README
3. Deploy a SecureCRDT server
4. Execute a workload from the Benchmark project by following its README

### Contact Us
If you are interested in this project or need support to deploy it, please feel free to [reach out](mailto:bernardo.portela@fc.up.pt,hpacheco@fc.up.pt,201706520@fc.up.pt,rogerio.a.pontes@inesctec.pt) to us. This project is maintained by:

- [Bernardo Portela](mailto:bernardo.portela@fc.up.pt)
- [Hugo Pacheco](mailto:hpacheco@fc.up.pt)
- [Pedro Jorge](mailto:201706520@fc.up.pt)
- [Rogério Pontes](mailto:rogerio.a.pontes@inesctec.pt)
