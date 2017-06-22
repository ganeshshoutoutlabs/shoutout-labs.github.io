### Integrate with ShoutOUT

Integrating with ShoutOUT is very easy. You have two options.

 1. [Use our client library to connect to our RESTful api](#cL)
 2. [Directly connect to our RESTful api](#rA)

### <a id="#cL"></a>Client Libraries

We maintain client libraries for several languages to connect to our RESTful API.

- [NodeJS](https://www.npmjs.com/package/shoutout-sdk)
- [PHP](https://packagist.org/packages/shoutoutlabs/shoutout-sdk)
- [Java](https://github.com/shoutout-labs/shoutout-sdk-java)

### <a id="#rA"></a>RESTful API

We have a very simple RESTful api with mainly three endpoints. And all three endpoints receives request data as JSON objects.

 1. [Create or update contact(s)](#1)
 2. [Create activity](#2)
 3. [Send message](#3)


#### <a id="#1"></a>Create or Update Contact(s)

**Sample curl command**

```curl
curl -X POST 
--header 'Content-Type: application/json' 
--header 'Accept: application/json' 
--header 'Authorization: Apikey <API_KEY>' 
-d '[{
        user_id: '94777123456',
        mobile_number: '94777123456',
        email: 'duke@test.com',
        name: 'Duke',
        tags: ['lead']
    }]' 'https://getshoutout.com/api/v8/contacts'
```

#### <a id="#2"></a>Create Activity

**Sample curl command**

```curl
curl -X POST 
--header 'Content-Type: application/json' 
--header 'Accept: application/json' 
--header 'Authorization: Apikey <API_KEY>' 
-d '{
        userId: '94777123456',
        activityName: 'Sample Activity',
        activityData: {
            param1: 'val1',
            param2: 'val2',
            param3: 'val3'
        }
    }' 'https://getshoutout.com/v8/activities'
```

#### <a id="#3"></a>Send Message

**Sample curl command**

```curl
curl -X POST 
--header 'Content-Type: application/json' 
--header 'Accept: application/json' 
--header 'Authorization: Apikey <API_KEY>' 
-d '{
        source: 'ShoutDEMO',
        destinations: ['94777123456'],
        content: {
            sms: 'Sent via SMS Gateway'
        },
        transports: ['sms']
    }' 'https://getshoutout.com/v7/messages'
```

### Questions or Problems ?

If you run into any difficulties or can't get something to work. Don't hesitate to contact us via <support@getshoutout.com>. We would love to help you out.

<small>Copyright © 2017. [ShoutOUT](https://getshoutout.com/) Labs. All Rights Reserved.</small>