Real Work Flow :-



Internet

&nbsp;  |

NACL (Inbound)

&nbsp;  |

Security Group (Inbound)

&nbsp;  |

EC2 Instance

&nbsp;  |

Security Group (Outbound)

&nbsp;  |

NACL (Outbound)



**Security group:**





A Security Group (SG) is a stateful virtual firewall that controls traffic at the resource level.



Applied to:



EC2 instances



ENIs



Load balancers



RDS, EKS nodes, etc.



📌 Think of SG as instance-level protection.



NACL:-



A Network ACL is a stateless firewall that controls traffic at the subnet level.



Applied to:



Entire subnets (public or private)



📌 Think of NACL as subnet-level protection.







Feature	        Security Group	           NACL

Scope	        Instance / ENI	         Subnet

Stateful	✅	                   ❌

Allow rules	✅	                   ✅

Deny rules	❌	                   ✅

Rule evaluation	 All rules evaluated	Lowest rule number wins



sudo apt update

sudo apt upgrade -y

sudo apt install apache2 -y

sudo systemctl start apache2

sudo systemctl enable apache2

sudo systemctl status apache2





Script :-



\#!/bin/bash

set -xe



\# Update package index

apt update -y



\# Install Apache2

apt install apache2 -y



\# Start Apache service

systemctl start apache2



\# Enable Apache to start on boot

systemctl enable apache2



\# Create a custom index page

echo "<h1>Apache2 Installed Successfully on Ubuntu EC2</h1>" > /var/www/html/index.html







