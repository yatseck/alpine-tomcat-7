#### Tomcat 7 image.
#### How to use:
* clone repository or:
* simple pull from docker hub
#### Simple run:
* docker run -d -P --name ~your_container_name~ yatsecksch/alpine-tomcat-7
#### to deploy app:
``` docker run -d -P \
-v patch/to/your/api.war:/srv/apache-tomcat-7.0.77/webapps/api.war \
--name your_container_name \
yatsecksch/alpine-tomcat-7```

#### it is possible to build image with your api.war deployed:
* add this directive into Dockerfile:
```COPY path/to/your/api.war /srv/apache-tomcat-7.0.77/webapps/api.war```
* and run your image

#### Credentials to manager:
```admin / p@$vv0Rd```

It is hardcoded in tomcat-users.xml & copied into container during the build
