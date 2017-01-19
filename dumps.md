ex300 dumps
Latest EX300 Exam Questions with PDF on store | 100% Free VCE Files

Exam Times:  RHCE: Two hours. 
Pass Scores:  Total 300 points. Pass at 210 points. 
Exam Environment:  Take examinations on a real system with a pre‐installed virtual machine.  All exams must be completed in the virtual 
machine.  Network must be well configured. If the network cannot be accessed, you will not  pass the exam.  In the iptables configuration, 
if you need to refuse the access, please use “Reject”.  (The default is set as ACCEPT.) 
Note:  Your IP address, Host Name, Gateway [ex300 dumps](http://www.lead4sure.com/ex300.html)and DNS has been configured.  IP address: 172.24.30.5/24  Hostname: station.domain30.
example.com  vim /etc/hosts  172.24.30.5 station.domain30.example.com  Add the corresponding relation between the host name and IP 
in the hosts records. 
You are a member of the domain30.example.com host domain, another domain is  t3gg.com‐‐‐172.25.0.0/16 network

QUESTION 1  To ensure SELinux open after the boot: 
Answer:   vim /etc/sysconfig/selinux  selinux=enforcing  setenforce 1  getenforce 

QUESTION 2  Open system kernel forwarding packets function: 
Answer:  vim /etc/sysctl.conf  net.ipv4.ip_forward = 1  sysctl ‐w (Effective immediately) 
The following commands should executed without sysctl.conf option:  sysctl ‐a |grep net.ipv4  sysctl ‐P net.ipv4.ip_forward = 1  
sysctl ‐w 

QUESTION 3  Configure SSH access as follows: 
 Harry has remote SSH access to your machine from within example.com   Clients within t3gg.com should NOT have access to ssh on your 
system 
Answer:  yum install ‐y sshd  chkconfig sshd on  vim /etc/hosts.deny  sshd: 172.25.0.0/16 
Use iptables:  iptables ‐F  iptables ‐X  iptables ‐Z  iptables ‐nvL  iptables ‐A INPUT ‐s 172.25.0.0/16 ‐p tcp ‐dport 22 ‐j REJECT  
services iptables save  Each finished writing a iptables rules saved 
