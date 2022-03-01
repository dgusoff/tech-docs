# cas on docker

```
FROM tomcat:8.0-alpine
LABEL maintainer="derek"

ADD sample.war /usr/local/tomcat/webapps/
ADD etc /usr/local/tomcat/bin
ADD cas.war /usr/local/tomcat/webapps/
ADD cas-management.war /usr/local/tomcat/webapps/

EXPOSE 8080
CMD ["catalina.sh", "run"]
```

`docker build -t cas-tomcat` 

`docker run -p 80:8080 cas-tomcat`
