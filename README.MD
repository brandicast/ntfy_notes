# ntfy notes

## Basic

 - website : https://ntfy.sh/
 - open source documents : https://docs.ntfy.sh/


## Self-host quick start notes  
   

### Server  
  
<br>  

&nbsp; via Docker  

<Br>


``` 
docker run -p 80:80 -it binwiederhier/ntfy serve
```

This pulls the image from Docker server and run on port 80


### Subscirber

#### <u>Mobile Devices</u>

- Download ntfy from App Store

- Update the server url to self host ip:port  
- specify the topic

    <b>Current (2025.04.04) client application supports 2 modes:
    1. json - Guess it's polling the server for new messages.  The apps warns about the battery usages and recommends with 2nd mode but need to make some changes on server configuration if the server is behind proxy.
    2. websocket - read https://docs.ntfy.sh/config/#nginxapache2caddy
    in the case of nginx, add the followings into conf: 

    <br>

    >

    ```
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
    ```
    
     </b>


### Publisher

#### <u>Windows CLI</u>

- Download the cli for windows as mentioned in the doc
- Send commands as the following

```
    ntfy send http://ip:port/topic "YOUR MESSAGE"
```    

<b><font color="red"> Do not add the trailing "/" in the tail of the url.  </font></b>

