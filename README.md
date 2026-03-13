Dataset Name
NIDS-28: Multi-Class Network Intrusion Detection Dataset

Kaggle Dataset Description
Title
NIDS-28 — Network Intrusion Detection Dataset (5-Class, KDD-Style)

Subtitle
A research-ready network intrusion detection dataset with 28 engineered features, 5 attack classes, and controlled class imbalance — designed for benchmarking deep learning and ensemble models.

About This Dataset
NIDS-28 is a network intrusion detection dataset inspired by the KDD Cup 1999 and NSL-KDD benchmarks. It was engineered to support deep learning research on multi-class attack classification and binary intrusion detection, with realistic class imbalance, overlapping class boundaries, and domain-faithful feature semantics.
The dataset was constructed as part of an end-to-end AI-based Network Intrusion Detection System (NIDS) research project, covering the full pipeline from raw traffic features through preprocessing, class balancing, deep learning model training, hybrid ensemble construction, and final evaluation.

Dataset Characteristics
Property
Value
Total Samples
28,000
Total Features
35 (30 numeric, 3 categorical, 2 label columns)
Input Features (after selection)
28
Classes (Multi-Class)
5
Classes (Binary)
2
Missing Values
None
File Format
CSV
Dataset Size
~13 MB


Class Distribution
Class
Label
Count
Percentage
Description
Normal
0
12,000
42.9%
Legitimate network traffic
DoS
1
8,000
28.6%
Denial of Service attack
Probe
2
4,000
14.3%
Surveillance and scanning attack
R2L
3
3,000
10.7%
Remote to Local attack
U2R
4
1,000
3.6%
User to Root privilege escalation

Imbalance ratio: 12:1 (Normal vs U2R), making it suitable for testing class balancing techniques such as SMOTE, ADASYN, and SMOTEENN.

Feature Description
Categorical Features
Feature
Type
Values
Description
protocol_type
Categorical
tcp, udp, icmp
Network protocol used
service
Categorical
http, ftp, smtp, ssh, dns, telnet, pop3, imap, other
Destination network service
flag
Categorical
SF, S0, REJ, RSTO, RSTOS0, SH, OTH
Connection status flag

Numeric Features
Feature
Type
Range
Description
duration
Float
0 – 58329
Length of connection in seconds
src_bytes
Float
0 – 114168
Bytes sent from source to destination
dst_bytes
Float
0 – 8759
Bytes sent from destination to source
wrong_fragment
Integer
0 – 3
Number of wrong fragments
urgent
Integer
0 – 3
Number of urgent packets
hot
Float
0+
Number of hot indicators
num_failed_logins
Integer
0 – 3
Number of failed login attempts
logged_in
Integer
0, 1
1 if successfully logged in
num_compromised
Float
0+
Number of compromised conditions
root_shell
Integer
0, 1
1 if root shell is obtained
su_attempted
Integer
0, 1
1 if su root command attempted
num_root
Float
0+
Number of root accesses
num_file_creations
Float
0+
Number of file creation operations
num_shells
Float
0+
Number of shell prompts
num_access_files
Float
0+
Number of operations on access control files
is_guest_login
Integer
0, 1
1 if login is a guest login
count
Integer
0 – 511
Connections to the same host in past 2 seconds
srv_count
Integer
0 – 511
Connections to same service in past 2 seconds
serror_rate
Float
0 – 1
% of connections with SYN errors
rerror_rate
Float
0 – 1
% of connections with REJ errors
same_srv_rate
Float
0 – 1
% of connections to the same service
diff_srv_rate
Float
0 – 1
% of connections to different services
srv_diff_host_rate
Float
0 – 1
% of connections to different hosts
dst_host_count
Integer
0 – 255
Count of connections to same destination host
dst_host_srv_count
Integer
0 – 255
Count of connections to same destination service
dst_host_same_srv_rate
Float
0 – 1
% of connections to same service on destination
dst_host_diff_srv_rate
Float
0 – 1
% of different services on destination host
dst_host_serror_rate
Float
0 – 1
% of connections with SYN errors on destination

Label Columns
Column
Type
Values
Description
attack_type
String
Normal, DoS, Probe, R2L, U2R
Multi-class attack label
binary_label
Integer
0, 1
Binary label — 0=Normal, 1=Attack


Intended Use Cases
Binary intrusion detection (Normal vs Attack)
Multi-class attack type classification

