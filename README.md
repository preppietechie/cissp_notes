# cissp_notes
Some last minute nodes I used in studying for the CISSP
Fixed width font is better for viewing. I may change the formatting to markdown someday for easier viewing. For now, just view the raw file.

ISO 27001: Auditing
ISO 27002: Best Practices (Formerly 17799)

Simple Security Property = No Read Up
//* Property = No Write Down
//Strong * Property = no read up/no write down
Simple=Read *=Write (easier to read than write)

Data Definition Language (DDL): Defines DB Schema
Data Manipulation Language (DML): search/modify DB contents

Bell-Lapadula = Military = confidentiality
Biba = Windows Update = integrity
Clark-Wilson = integrity
Brewer-Nash/Chinese Wall = protects from conflict of interest (Chinese brewed tea)
"i" in the name = integrity

Orange Book:
------------
Minimal
Discretionary
Mandatory
Verified

Common Criteria:
----------------
Evaluation Assurance Level (EAL)
EAL 1 = Functionally Tested
EAL 2 = Structurally Tested
EAL 3 = Methodically Tested + Checked
EAL 4 = Methodically Designed, Tested + Checked
EAL 5 = Semi Formally Designed + Tested
EAL 6 = Semi Formally Verified, Designed + Tested
EAL 7 = Formally Verified, Designed + Tested

EAL 1 = Lowest assurance
EAL 7 = Highest assurance

Memory Addressing:
------------------
Direct
Register Direct
Indirect (Pointer)
Register Indirect
Index

Database Models:
----------------
Hierarchical
Mesh
Object-Oriented
Relational

DES
---
56 bit key size
64 bit block size
DES Modes: 
	Electronic Codebook (ECB) (weakest)
	Cipher Block Chaining (CBC)
	Output Feedback (OFB)
	Cipher Feedback (CFB)
	Counter Mode (CTR)

AES
---
Rijndael
128 bit block size
Variable key size 128, 192, 256
AES Functions:
	SubBytes
	ShiftRows
	MixColumns
	AddRoundKey
AES Finalists:
	Rijndael
	MARS
	RC6
	Serpent
	Twofish

Symmetric = Faster than Asymmetric
DES is 100x faster than RSA

Symmetric:
----------
DES
AES
Blowfish
Twofish
IDEA
RC4,5,6

Asymmetric:
-----------
RSA
Diffie-Hellman
Elliptic Curve (strongest and lower power Asymmetric enc.)

HASH:
-----
SHA
MD5

Fences:
-------
3-4ft/1m (deterrent)
6-7ft/1m
8ft/2.4m + 3 strands barbed wire (preventative)

Gates:
------
Class I = residential
Class II = commercial
Class III = industrial
Class IV = restricted access

Lights:
-------
Must be 8ft/2.4m w/2 candle power

Relative Humidity = 40% to 60%
Temperature rage = 70-74°F / 21-23°C

Fire Classes:
-------------
A = ash = Wood (water/soda acid)
B = bubble/boil = Liquids/Petroleum (Halon/CO2/soda acid)
C = circuit = electrical (Halon/CO2)
D = dent = combustible metals (dry powder)

Fire Suppression:
----------------
CO2/Soda Acid = Remove oxygen
Water = removes temperature
Gas (halon) interferes w/chemical reactions

Sprinkler Filament melts @ 165°F

Montreal Protocol (1987) Banned Halon production

----OSI-----------------TCP------------
|Application  |                       |
|-------------|                       |
|Presentation | Application           |
|-------------|                       |
|Session      |                       |
|-------------|-----------------------|
|Transport    | Host to Host Transport|
|-------------|-----------------------|
|Network      | Internet              |
|-------------|-----------------------|
|Data Link    |                       |
|-------------| Network               |
|Physical     |                       |
---------------------------------------
"Please do not throw sausage pizza away"

DNS Queries:
------------
gethostbyname
gethostbyaddr

UDP Ports:
----------
DNS (53)
NTP (123)
BOOTP (67 and 68)
TFTP (69)
SNMP (161)

TCP PORTS:
----------
FTP Data (20)
FTP Server (21)
SSH (22)
Telnet (23)
SMTP (25)
DNS (53)
finger (79)
HTTP (80)
LDAP (389)
HTTPS (443)
Ephemeral (1024 and up)
RDP (3389)
VNC (5900)

Protocol Numbers:
-----------------
TCP=6
UDP=17

TCP/UDP Ports:
--------------
0-65535

TCP Code Bits:
--------------
URG
ACK
PSH
RST
SYN
FIN

DNP3:
-----
Multilayer Scada Protocol
IEEE 1815-2012 (nee 1815-2010)

Leased Lines:
-------------
T1:DS1 1.544
T3:DS3 44.736
E1 2.048
E3 34.368

SDLC and HDLC:
--------------
Normal Response Mode (NRM): primary initiates.
Asynchronous Response Mode (ARM): secondary can initiate, primary owns recovery, link setup/term.
Asynchronous Balanced Mode (ABM): primary and secondary are equals. full duplex. X.25

ISDN:
-----
two 64k channels

DSL:
----
  SDLS =  1.544M
  HDLS =  1.544/2.048M (2pair)
 SHDSL =  5.696M
 ADSL2 =  12M🠗/3.5M🠕
ADSL2+ =  24M🠗/3.5M🠕
 VDSL3 =  52M🠗/16M🠕
 VDLS4 = 100M🠗/100M🠕 (@1600ft)
ATM:
----
Cell Size = 48 bytes data / 5 bytes header
 
Coaxial:
--------
50ohm cable - digital signaling
75ohm cable - high speed data and analog
 
UTP:
----
CAT1 = telephone wire
CAT2 = 4m
CAT3 = 10m
CAT4 = 16m
CAT5 = 100m
CAT5e/6 = 1000m

Routing:
--------
RIP = Distance Vector
OSPF = Link State
BGP = Exterior Gateway Protocol

"Tunnel" or "Encryption ≠ confidentiality

TACACS:
-------
TCP based
single factor

RADIUS:
-------
UDP based

EAP:
----
EAP-MD5: no mutual auth, weakest
EAP-TLS: requires client certs/pki
EAP-TTLS: allows PSK instead of client certs
PEAP: Cisco/MS/RSA response to EAP-TTLS

AAA:
----
Identity
Authentication
Authorization
Accountability

Password Attacks:
-----------------
Dictionary: wordlist
Hybrid Attack: wordlist + add/change characters
Brute Force: every possible pw
Rainbow Table: table of pre-computed hashes

Biometrics:
-----------
Crossover Error Rate = When FRR=FAR
FRR = Type 1
FAR = Type 2
Enrollment < 2 min
Throughput > 10/min

Kerberos:
---------
v4=DES
v5=TDES + RC4
KDC: access to all keys, issues TGTs
TGS: issues service tickets
Key Benefit: mutual authentication

AD is LDAP v3 compliant

Access Control Models:
----------------------
MAC
DAC
Non-Discretionary (RBAC/ABAC)

IDS Events:
-----------
True Positive  =     is malicious / IDS alerts
True Negative  = is not malicious / IDS doesn't alert
False Positive = is not malicious / IDS alerts
False Negative =     is malicious / IDS doesn't alert

Incident Handling:
------------------
Preparation
Detection
Response
Mitigation
Reporting
Recovery
Remediation
Lessons Learned

"Please Don't Read My Really Really Really Longnemonic"

Types of Evidence:
------------------
Physical/Real
Direct Testimony
Circumstantial Testimony
Expert Testimony
Documentary
Corroborating

Rules of Evidence:
------------------
Data records are hearsay except:
Routinely used business records (Rule 803)
Forensic Disk/Ram images (Rule 1001)

RAID:
-----
RAID 0 = Striping, no redundancy
RAID 1 = *Mirroring, fully redundant
RAID 2 = Obsolete, bit interleaved, hamming code
RAID 3 = Dedicated parity, byte level striping
RAID 4 = Dedicated parity, block level striping
RAID 5 = *Distributed parity, block level striping
RAID 6 = Double distributed parity, block level striping
*common

Recovery:
---------
BIA determines: max allowable downtime
MTD=how long can we afford to be down
RTO=how long to recover hw/sw
WRT=how long until business work resumes
RPO=how much data can we lose?
MTD=RTO+WRT

Alternate Sites:
----------------
Multiple Processing Sites
Hot
Warm
Cold
Hybrid
Mobile
Reciprocal

Safety Warden = "get out"
Meeting Point Leader = headcount

CMMI:
-----
Level 1 - Initial
Level 2 - Managed
Level 3 - Defined
Level 4 - Quantitatively Managed
Level 5 - Optimizing

Software Development Methodologies:
-----------------------------------
Waterfall
Spiral
Prototyping
Rapid Application Development (RAD)
Agile
Extreme Programming (XP)
Scrum
