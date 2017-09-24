# OpenIAM
Let's see what can I do with OpenIAM. (Sometimes it even confuses me : OpenIAM or OpenAIM :p) . 

### Connect to AWS
`ssh -i "RedHat.pem" ec2-user@ec2-35-167-153-106.us-west-2.compute.amazonaws.com`

### Download OpenIAM Distributions
`wget http://www.openiam.com/downloads/builds/rpm/3.5/openiam-3.5-BUILD.20170313.x86_64.rpm`

Before proceeding make sure that you have java 7, mysql and tomcat installed.

### Setup Mysql

* change mysql root password : `sudo nano /usr/local/OpenIAM/utility/createDatabase/mysql/mysql.properties`
* create DB for OpenIAM `./usr/local/OpenIAM/utility/createDatabase/mysql/create.sh`

### Run backend
`sudo service jbossas7 start`
`sudo service jbossas7 log`

###
