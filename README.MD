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


### Publisher

#### <u>Windows CLI</u>

- Download the cli for windows as mentioned in the doc
- Send commands as the following

```
    ntfy send http://ip:port/topic "YOUR MESSAGE"
```    


