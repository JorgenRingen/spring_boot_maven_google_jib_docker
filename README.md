# Spring Boot + Maven + JIB + Docker

Using [Google Jib](https://github.com/GoogleContainerTools/jib)
to build and publish docker container.

**Usage**

Build application
```
mvn package
```

Create Dockerfile (optional)
```
mvn jib:exportDockerContext
```

Publish docker container to registry
```
mvn jib:build
```

Docker registry and authentication can be configured in several ways. 

Dockerhub is the default registry (remember to create repository). 

Username/password can be provided in settings.xml, command-line arguments or credential helpers. 
See [this](https://github.com/GoogleContainerTools/jib/tree/master/jib-maven-plugin#authentication-methods)
link for more info.