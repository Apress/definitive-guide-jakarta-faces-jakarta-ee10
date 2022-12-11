# Errata for *The Definitive Guide to Jakarta Faces in Jakarta EE 10*

On **page xx** [Summary of error]:
 
Details of error here. Highlight key pieces in **bold**.

***

On **page xx** [Summary of error]:
 
Details of error here. Highlight key pieces in **bold**.

***

On **page 38** web.xml checking fails:
 
When using the configuration detailed in the book:
```
<web-app 
        xmlns="https:/jakarta.ee/xml/ns/jakartaee" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xsi:schemaLocation="https://jakarta.ee/xml/ns/jakartaee https://jakarta.ee/xml/ns/jakartaee/web-app_6_0.xsd" 
        version="6.0"
>
```

Eclipse's XML-checker complaints: 

> cvc-elt.1.a: Cannot find the declaration of element 'web-app'.

Instead of using the configuration in the book, the following seems to work. 
(But I have to admit, I am not sure why the above fails and why the solution below works):

```
<web-app
        xmlns = "https://jakarta.ee/xml/ns/jakartaee"
        xmlns:xsi = "http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation = "https://jakarta.ee/xml/ns/jakartaee https://jakarta.ee/xml/ns/jakartaee/web-app_6_0.xsd"
        version = "6.0"
        metadata-complete = "false"
>
```

***
