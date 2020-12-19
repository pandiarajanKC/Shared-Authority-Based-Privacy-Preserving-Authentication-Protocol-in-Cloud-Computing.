# Shared-Authority-Based-Privacy-Preserving-Authentication-Protocol-in-Cloud-Computing.
Shared Authority Based Privacy-Preserving Authentication Protocol in Cloud Computing.

Demo : http://freesourcecoder.com/shared-authority-based-privacy-preserving-authentication-protocol-in-cloud-computing

Description:
Using Cloud Storage, users can remotely store their data and enjoy the on-demand high quality applications and services from a shared pool of configurable computing resources, without the burden of local data storage and maintenance. However, the fact that users no longer have physical possession of the outsourced data makes the data integrity protection in Cloud Computing a formidable task, especially for users with constrained computing resources. Moreover, users should be able to just use the cloud storage as if it is local, without worrying about the need to verify its integrity. Thus, enabling public auditability for cloud storage is of critical importance so that users can resort to a third party auditor (TPA) to check the integrity of outsourced data and be worry-free. To securely introduce an effective TPA, the auditing process should bring in no new vulnerabilities towards user data privacy, and introduce no additional online burden to user. In this paper, we propose a secure cloud storage system supporting privacy-preserving public auditing. We further extend our result to enable the TPA to perform audits for multiple users simultaneously and efficiently. Extensive security and performance analysis show the proposed schemes are provably secure and highly efficient. Our preliminary experiment conducted on Amazon EC2 instance further demonstrates the fast performance of the design.

 

ALGORITHM:

A public auditing scheme consists of four algorithms (KeyGen, SigGen, GenProof, VerifyProof).

KeyGen: key generation algorithm that is run by the user to setup the scheme
SigGen: used by the user to generate verification metadata, which may consist of MAC, signatures or other information used for auditing
GenProof: run by the cloud server to generate a proof of data storage correctness
VerifyProof: run by the TPA to audit the proof from the cloud server
MODULES: 

Cloud Setup:  

To fully ensure the data integrity and save the cloud users’ computation resources as well as online burden, it is of critical importance to enable public auditing service for cloud data storage, so that users may resort to an independent third party auditor (TPA) to audit the outsourced data when needed. The TPA, who has expertise and capabilities that users do not, can periodically check the integrity of all the data stored in the cloud on behalf of the users, which provides a much more easier and affordable way for the users to ensure their storage correctness in the cloud.     

 Privacy-Preserving Public Auditing Module: 

Holomorphic authenticators are unforgeable verification metadata generated from individual data blocks, which can be securely aggregated in such a way to assure an auditor that a linear combination of data blocks is correctly computed by verifying only the aggregated authenticator. Overview to achieve privacy-preserving public auditing, we propose to uniquely integrate the holomorphic authenticator with random mask technique. In our protocol, the linear combination of sampled blocks in the server’s response is masked with randomness generated by a pseudo random function (PRF).

                     The proposed scheme is as follows:

Setup Phase
Audit Phase 
Batch Auditing Module:

 With the establishment of privacy-preserving public auditing in Cloud Computing, TPA may concurrently handle multiple auditing delegations upon different users’ requests. The individual auditing of these tasks for TPA can be tedious and very inefficient. Batch auditing not only allows TPA to perform the multiple auditing tasks simultaneously, but also greatly reduces the computation cost on the TPA side.

 Data Dynamics Module: 

Supporting data dynamics for privacy-preserving public risk auditing is also of paramount importance. Now we show how our main scheme can be adapted to build upon the existing work to support data dynamics, including block level operations of modification, deletion and insertion. We can adopt this technique in our design to achieve privacy-preserving public risk auditing with support of data dynamics.

