# OpenIAM
Let's see what can I do with OpenIAM. (Sometimes it even confuses me : OpenIAM or OpenAIM :p) . 

### Connect to AWS
ssh -i "RedHat.pem" ec2-user@ec2-35-167-153-106.us-west-2.compute.amazonaws.com

### Download OpenIAM Distributions
wget http://www.openiam.com/downloads/builds/rpm/3.5/openiam-3.5-BUILD.20170313.x86_64.rpm

Before proceeding make sure that you have java 8 installed. Otherwise install the same . you may follow these guidelines to  install java 8 - [here](https://tecadmin.net/install-java-8-on-centos-rhel-and-fedora/)

### Run backend
sudo service jbossas7 start

###
