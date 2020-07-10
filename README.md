# Web-Application-Security

### Browser Basics

The browser is a rendering engine. Its job is to download a web page and render it in a way that’s understandable to a human being.

Brower Job is 

### DNS Resolution
It will make sure that when user enters URL , browser will know which server to connect to.If Users enters google.com , browser contacts DNS server to resolve the IP address

### HTTP Exchange

Once browser identifies which server to connect to, it makes TCP connection and makes HTTP exchange.
HTTP is generally a protocol for web.
HTTP exchange involves a client -> sending request and server -> sending response.

   ### parsing sample request
     Once browser connects to server , then browser will make request.
     
     GET / HTTP/1.1
     Host: google.com
     Accept: */*
     
     Browser is asking for retreiving a document at location '/'. HTTP/1.1 is protocal and version can be anything 1.0 , 2.
     
     Host: google.com - It is the mandatory header in 1.1 , as domain have google.com,goggle.co.uk , Browser specifying from .com
     
     Accept: */* - Browser will accept any kind of resource , JSON,HTML ,text etc ...
     
  ### parsing sample response
  
    sample server response
    
    HTTP/1.1 200 OK
    Cache-Control: private, max-age=0
    Content-Type: text/html; charset=ISO-8859-1
    Server: gws
    X-XSS-Protection: 1; mode=block
    X-Frame-Options: SAMEORIGIN
    Set-Cookie: NID=1234; expires=Fri, 18-Jan-2019 18:25:04 GMT; path=/; domain=.google.com; HttpOnly

    <!doctype html><html">
    ...
    ...
    </html>

### How a browser renders an HTTP response

Server includes representation of response in content-type : text/HTML
and browser renders this response as HTML.

For details visit :  https://github.com/alex/what-happens-when

Security is very important ,
whenever user enters credit card details , hacker can hack it without even reaching server.









