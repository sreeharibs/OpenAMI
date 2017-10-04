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

### Creating Organization

head on to http://35.198.247.142:8080/webconsole ==> user admin ==> organization ==> create new organization

## Playing with REST

### Create User

* 

### Reset Password

* POST : http://35.198.247.142:8080/webconsole/rest/api/prov/resetPassword 

* BODY : 
`{"userId": "8a1480825ee0aa2c015ee718bfbe00fb",  
"password": "pass@123",  
"confPassword": "pass@123",  
"managedSystem": [0] }`



### Create User
* BODY :
`{
        "id": null,
        "userStatus": "ACTIVE",
        "secondaryStatus": null,
        "firstName": "Manish",
        "middleInit": null,
        "lastName": "Jain",
        "nickname": null,
        "maidenName": null,
        "suffix": null,
        "prefix": null,
        "sex": "M",
        "showInSearch": 1,
        "title": "Asst Manager",
        "jobCodeId": "MANAGER",
        "classification": "classification",
        "employeeId": "u1010",
        "userTypeInd": null,
        "employeeTypeId": "SYS ACCOUNT",
        "metadataTypeId": "DEFAULT_USER",
        "emails":
        [
         {
                "operation": "ADD",
                "email": "sreehari.bs@ospyn.com",
                "typeId": "PRIMARY_EMAIL",
                "description": "description",
                "default": true,
                "active": true
            }
        ],
        "addresses":
        [
            {
                "operation": "ADD",
                "active": true,
                "default": true,
                "bldgNumber": "tc 36/215",
                "address1": "Vetturoad Lane",
                "address2": "Thiruvananthapuram",
                "city": "Trivandrum",
                "postalCd": "695001",
                "state": "Kerala",
                "typeId": "HOME_ADDRESS",
                "country": "India",
                "description": "Address description"
            }
        ],
        "phones":
        [
            {
                "operation": "ADD",
                "active": true,
                "default": true,
                "typeId": "OFFICE_PHONE",
                "areaCd": "0471",
                "phoneExt": "1",
                "phoneNbr": "8075943776",
                "countryCd": "91",
                "description": "Phone description"
            }
        ],
        "notifyUserViaEmail": true,
        "notifySupervisorViaEmail": false,
        "provisionOnStartDate": false,
        "organizationIds":
        [
         {
                "id": "ddfsv04"
            }
        ],
        "userSubTypeId": "FULL_TIME",
        "partnerName": "pnn",
        "prefixPartnerName": "ppn",
        "prefixLastName": "la",
        "companyOwnerId": null,
        "roleList":
        [
        {
                "id": "5",
                "operation": "ADD"
            }
        ],
        "groupList":
        [
        {
                "id": "SUPER_SEC_ADMIN_GRP",
                "operation": "ADD"
            }
        ],
        "userAttributes":
        {
         "attr1":
            {
                "name": "attr1",
                "value": "attr1111",
                "operation": "ADD"
            },
        "attr2":
            {
                "name": "attr2",
                "value": "attr222",
                "operation": "ADD"
            }
 
        },
        "resources":
        [
            {
                "id": "111",
                "operation": "ADD"
            }
        ],

        "notProvisioninResourcesIds": null,
        "emailCredentialsToNewUsers": false,
        "addInitialPasswordToHistory": false,
        "skipPreprocessor": false,
        "skipPostProcessor": false,
"password":"pass@123",
"confirmPassword":"pass@123"

    }`
