# Docker

----------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------

# How to deploy springboot application on docker?


  1) create build (.jar) of your springboot application using this command->
     
     - mvn clean install -DskipTests
      - this will create a package of your application. having name with .jar extension.

  2) create Dockerfile on same directory -> with name Dockerfile
     - copy all code and paste it on your Dockerfile
       
        - FROM openjdk
        - COPY ./target/*.jar springboot-application.jar
        - ENTRYPOINT [ "java","-jar","/springboot-application.jar" ]
        
  3) Build Docker Image ->
  
     - docker build -t nameforapp .
     
  4) Run Image ->
  
     - hit cmd -> docker images
       check image and use image-id for run image 
      
     - docker run --name nameforcontainer put-image-id
    
