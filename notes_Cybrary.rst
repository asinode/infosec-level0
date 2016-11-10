D| 9 Nov 2016
Notes During Cybrary's Course - ENTRY LEVEL CYBER SECURITY ANALYST
==================================================================

Introduction
------------

Begins with Chapter-2: Asset Security. Not sure where the Chapter-1 discussion is. Maybe I should try forums.

AGENDA in this chapter:
* Roles within Organization
* Classification of Data
* System Baselining and Hardening
* States of Data

Roles and Responsibilities
--------------------------

Sr Executive Management
* CEO
* CFO
* CIO
* Information Security Officer ISO: Risk Analysis and Mitigation
* Steering Committee: Define risks, objectives, approaches
* Auditors: Evaluate business processes
* Data Owner: Classifies data
* Data Custodian: Day to day maintenance of data, backing up, etc.
* Network Admin: Ensures Availability of network resources
* Security Admin: Reposnsible for all security-related tasks, focusing on Confidentiality and Integrity

ISO
---

* Responsible for providing C-I-A for all information assets.
* Communication of risks to senior management
* Recommends best practices to influence policies, standards, procedures, guidelines
* Establish security measurements
* Ensure compliance with government and industry regulations
* Maintains awareness of emerging threats

Data Classification
-------------------

What types of controls are necessary for a particular data -- this is all about classification!

Confidential, top secret, secret, classified, etc. are the terms used in this case.

They are like sensitivity labels for data and those labels help define the baseline security to be provided to them based on the value of the data.

So Cost::Value of Data plays an important role. Very important!

Once you know the value of the data, you will give the label, meaning you will classify the data based on the criteria meant for each class/label.

Determining the baseline security to be provided to a particular class/label, this step is called setting CONTROLS.

Data Owner determines the classification of data.

Data Custodian maintains the data.

Asset Valuation
---------------

What makes up the value of an asset?
	- Value to the org
	- Loss if compromised
	- Legislative drivers
	- Liabilities
	- Value to competitors
	- Acquisition costs
	- And many others
	
Sensitivity Vs Criticality
--------------------------

Sensitivity -- describes the amount of damage that would be done should the information be disclosed. It is about privacy. To be or not to be disclosed! 

Criticality -- describes the time sensitivity of data. This is usually driven by the understanding of how much revenue a specific asset generates, and without that asset, there will be lost revenue.

States of Data
-------------

At Rest -- File system encryptions, EFS, TPM -- this is static, not manipulated, just stored.
	- Windows used Encrypted File System (EFS). This is owned by Windows and not a third party tool, which is an important point to remember. 
	- EFS may not fully protective if somebody got the hard disk and tried to open it in a linux system. 
	- EFS does protect the data even in this case, but only to an extent. 
	- Linux guy will still be able to find the timestamps of files, file names, and much more. This is the disadvantage of using OS-specific encryption systems.

Trusted Platform Modules (TPM) -- is created exactly to address this disadvantage. 
	- Each motherboard bought in the last 10 years comes with a TPM chip. What it does is -- the whole drive encryption. 
	- So it locks the entire hard drive, store the key to decrypt the drive on this chip, so if you remove the hard drive, it cannot access the key required to unlock the drive. So more protection!
	- Explore about BitLocker technology, PGP .... these can do the 'locking of entire drive'. 
	- The necessary keys don't have to be necessarily on the TPM chip, you can store it wherever you want it but ensure it is safe.

In Process -- This is basically when you are doing some work with the data within your computer. 
	- In this case, there is nothing particular in terms of protection. Best practices like, never leave your system unlocked, etc. are the only means by which you can protect this data.

In Transit -- This is very crucial because the data is out on the network somewhere. Essentially, it is out of your hands.
