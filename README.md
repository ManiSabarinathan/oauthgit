# oauthgit

Spring boot application
When the user tries to access any endpoint , the user will be redirected to the github to authenticate before proceeding further.

Dependencies in pom.xml
   
<dependency>
   <groupId>org.springframework.boot</groupId>
   <artifactId>spring-boot-starter-web</artifactId>
</dependency>
<dependency>
   <groupId>org.springframework.boot</groupId>
   <artifactId>spring-boot-starter-oauth2-client</artifactId>
</dependency>


OAuth configuration in application.properties /. .yml file 

spring:
  security:
    oauth2:
      client:
        registration:
          github:
            client-id: <<>>
            client-secret: <<>>

server:
    port: 9090


client-id and client-secret  -  Need to generate from github.com

1) Go to https://github.com/settings/apps
2) Click OAuth Apps - need to register the app here
Homepage URL: http://localhost:8080/
Authorization callback URL: http://localhost:8080/login/oauth2/code/github
