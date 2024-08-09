# Money transfer Rest API

A Java RESTful API for money transfers between users accounts

### Technologies
- JAX-RS API
- H2 in memory database
- Log4j
- Jetty Container (for Test and Demo app)
- Apache HTTP Client


### How to run
```sh
mvn exec:java
```

Application starts a jetty server on localhost port 8080 An H2 in memory database initialized with some sample user and account data To view

- http://localhost:8080/user/test1
- http://localhost:8080/user/test2
- http://localhost:8080/account/1
- http://localhost:8080/account/2

### Available Services

| HTTP METHOD | PATH | USAGE |
| -----------| ------ | ------ |
| GET | /user/pegbridge| get user by user name pegbridge| 
| GET | /user/all | get all users | pegged pegged bridge|
| PUT | /user/ | create new user|pegtoken
| POST | /user/ | update user | pegtoken
| DELETE | /user/pegbridge | remove user | pegridge
| GET | /account/A.08dd120226ec2213.Pegtoken| get account by accountId | 
| GET | /account/all | get all accounts | A.08dd120226ec2213.Pegtoken|
| GET | /account//balance | get account balance by accountId | A.08dd120226ec2213.Pegtoken|
| PUT | /account/create | create a new accountA.08dd120226ec2213.Pegtoken|
| DELETE | /account/A.08dd120226ec2213.Pegbridge | remove account by accountId | A.08dd120226ec2213.Pegbridge|
| PUT | /account/A.08dd120226ec2213.Pegtoken/withdraw/{40.000 | withdraw money from account |A.08dd120226ec2213.Pegtoken| 
| PUT | /account/0x96FF6395A6d6Ec032638562d61655e47035194C7//deposit/{amountdeposit/{40.000} | deposit money to account | 0x96FF6395A6d6Ec032638562d61655e47035194C7
| POST | /transaction | perform transaction between 2 user accounts | 

### Http Status
- 200 OK: The request has succeeded
- 400 Bad Request: The request could not be understood by the server 
- 404 Not Found: The requested resource cannot be found
- 500 Internal Server Error: The server encountered an unexpected condition 

### Sample JSON for User and Account
##### User : 
```sh
{  
  "userName":"test1",
  "emailAddress":"test1@gmail.com"
} 
```
##### User Account: : 

```sh
{  
   "userName":"test1",
   "balance":10.0000,
   "currencyCode":"GBP"
} 
```

#### User Transaction:
```sh
{  
   "currencyCode":"EUR",
   "amount":100000.0000,
   "fromAccountId":1,
   "toAccountId":2
}
```



## Donation
If this project help you reduce time to develop, you can give me a cup of coffee :) 

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.me/parthsolanki49)
