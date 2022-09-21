# State-Machine-Solutions-Documentation

If this project helps you, please donate

# Donate:
https://www.paypal.com/donate/?hosted_button_id=TX922XCPET8QG

![donation qrcode image](https://github.com/state-machine-solutions/State-Machine-Solutions-Documentation/blob/main/donations_QRcode.png?raw=true)

## Documentation References


### Run

```
node server
```

### Config example

```
{
    "appName":"Example",
    "connections":{
        "http":{
            "port":8001
        },
        "https":{
            "port":8002,
            "key":"",
            "cert":""
        },
        "io":{
            "port":8000,
            "auth":{
                "username":"test",
                "password":"passtest"
            }
        },
        "cors":{
            "origin": "*"
        }
    },
    "attached":[],
    "initialData":"./initialData.json",
    "__validation":"./validation.json",
    "hidePanel":false,
    "measureBytes":true
}

```

Config with comments:

```

{
    "appName":"Example", // The label
    "connections":{
        "http":{
            "port":8001 // http port used to communicate, remove http node to do not listen http port
        },
        "https":{ // to ssl https
            "port":8002, // port
            "key":"", // path to cert file
            "cert":"" // path to cert file
        },
        "io":{
            "port":8000, //socket.io port to listen
            "auth":{ // optional, make it null if you dont wanna authentication
                "username":"test", // user
                "password":"passtest" // password, the same for all users
            }
        },
        "cors":{
            "origin": "*" // try to permit cors
        }
    },
    "attached":[], 
    "initialData":"./initialData.json", // wherever you put here, in json, when the app starts, they will start with this data values
    "__validation":"./validation.json", // to validate schema, it makes the communication more slow
    "hidePanel":false, // dont show console log panel
    "measureBytes":true
}

```
