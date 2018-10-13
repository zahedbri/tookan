# **Tookan**
[Tookan](https://gitlab.com/npm-package-jilabaji/tookan), this project is to intract the application with tookan API's 
this lib us using v2 of tookan to intagrate with you can find the API on following link https://tookanapi.docs.apiary.io

## **Config the tookan library**
Set the environment variable where we keep the tookan key and the tookan user id 
the params are following
> tookan_key
> tookan_userid

## **Install**
> npm  i  tookan

## **Initialization**
A simple example to create client
` let Tookan_help = require("tookan"); `

## **All Functions**
###  Get all agents available 
just call this method to get the available agents in our tookan
> tookan_res = await Tookan_help.get_agents() 

###  Create a Delivery Task 
Create a payload as follows

```
 let payload = {
        order_id: "1582325102",
        job_description: "Its a delivery order for testing the tookan delivery network",
        job_delivery_phone: "19999999999",
        job_delivery_datetime: "09/01/2018 19:00:01",
        job_delivery_address: "Big Streeet, North Earth, Galaxy unknown",
        customer_username: "Mark",
        customer_email: "mark@unknown.com",
    } 
```
And send this payload to a tookan
> tookan_res = await Tookan_help.create_delivery(payload) 

###  Create a Delivery Task 
Create a payload as follows

```
  let payload_pickup = {
        order_id: "1582325101",
        job_description: 'Its a delivery order for testing the tookan delivery network',
        job_pickup_phone: "19999999999",
        job_pickup_datetime: "09/01/2018 19:00:01",
        job_pickup_address: "Big Streeet, North Earth, Galaxy unknown",
        job_pickup_name:  "Mark",
        job_pickup_email: "mark@unknown.com",
    } 
```

And send this payload to a tookan
> tookan_res = await Tookan_help.create_pickup(payload) 

###  Check the task by its job id 
Create a payload as follows

```  let payload = {
        'job_id':"61112352",
    } 
```
And send this payload to a tookan
> tookan_res = await Tookan_help.check_task(payload) 

###  Check the task by its job id 
Create a payload as follows

```  let payload = {
        'order_id':"1582325102",
    } 
```

And send this payload to a tookan
> tookan_res = await Tookan_help.check_task_by_orderid(payload)