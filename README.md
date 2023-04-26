# Super
en 
conf t
router ospf 1
network 192.168.1.0 0.255.255.255 area 1
network 192.168.2.0 0.255.255.255 area 1
exit

en 
conf
interface gigabitEthernet 0/0 
ip ospf authentication message-digest
ip ospf message-digest-key 1 md5 smile
exit
exit

en 
show ip ospf interface gigabit 0/1


R1AndR2
en 
show clock

R1Andr2
conf t
ntp server 192.168.1.3
ntp update-calendar
exit

R2AndR1
en
conf t
logging to 192.168.1.2
exit

////AAA\\\ 

Go t
service aaa on
Akash 192.168.2.1
abcd scret
tax

user
akash 1234
 add

2radius
service 
aaa on 
Akash 192.168.2.1
abcd scret
ra
akash 1234

r1
en
conf t

aaa new-model
tacacs-server host 192.168.2.3 key abcd
radius-server host 192.168.2.2 key abcd
aaa authentication login akash group tacacs+ group radius local
line vty 0 4
login authentication akash
exit


telnet 192.168.2.1

akash
1234


shutdown

same

