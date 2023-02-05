# SMW Lecture 7 - Planning and Deploying Public Key Infrastructure and Secured Web Content Web Services

###### tags: #SMW 

## Table of Contents
```toc
```

## Defining Certificate Requirements
- Windows Server enables secure data access based on the use of digital certificates
- Certificates allow users or systems to prove to others that they are who they say they are
- Before you can use digital certificates, a Public Key Infrastructure (PKI) needs to be designed
- **To protect exchange messages from eavesdropping attack with asynchronous encryption algorithms**
	- A key-pair is associated with an individual party
	- Each individual party will keep its private key as a secret but share out its public key to everyone
	- Messages being encrypted with the public key can only be decrypted by the corresponding private key
	- Digitally signed message with the individual private key can only be verified by its corresponding public key
	- **Concern**
		- How can we obtain a genuine public key of a particular party before we can establish a secure communication channel with the party
- **Public Key Infrastructure**
	- Refers to a technology that includes a series of features relating to authentication and encryption
	- Based on a system of certificates, each certificate contains a public key and the name of the subject
	- Allows an organisation to publish, use, renew or revoke certificates and enrol clients
- Certificates may be required if you are using any of the following applications:
	- Digital signatures
	- Secured email
	- HTTPS/SSL
	- Internet authentication
	- Software code signing
	- IP security
	- Smart card logon
	- Encrypted file system
	- 802.1x authentication

## Certificate Authority
> An entity that issues digital certificates to other parties

- Root CA can issue certificates to SubOrdinate, Immediate or Issuing CAs
- Issuing CAs can issue certificates to users or clients

### Certificate Authority Hierarchies and Roles
- Types of hierarchies that can be used for CAs:
	- Rooted trust model
	- Cross-certification trust model
	- Hybrid trust model
- Roles that can be chosen for CAs:
	- **Standalone CA**
		- Rudimentary CA
		- Intermediate CA
	- **Enterprise CA**
		- Basic Security CA
		- Medium Security CA
		- High Security CA

> Notes:
> - For Standalone CA setup, target clients are not bound to the enterprise which implements the service
> 	- Applicable for offering to the general public
> - Enterprise CA setup, its target clients are within the enterprise
> 	- Suitable for 