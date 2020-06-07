# clouderamanager-install
from https://community.cloudera.com/t5/Support-Questions/Cloudera-manager-embedded-database-fails-to-come-up/td-p/92290

1. sed -i 's/SELINUX=enforcing/SELINUX=permissive/' /etc/selinux/config

2. hostnamectl set-hostname master1.hadoop-test.com

echo "10.99.0.175 master1.hadoop-test.com master1" >> /etc/hosts

sed -i 's/\r//' /etc/hosts

echo "HOSTNAME=master1.hadoop-test.com" >> /etc/sysconfig/network

3. reboot

4. wget https://archive.cloudera.com/cm6/6.3.1/cloudera-manager-installer.bin

5. chmod u+x cloudera-manager-installer.bin

6. ./cloudera-manager-installer.bin
