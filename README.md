# Simple-SpringBoot-Application

step 1 :  create a maven project in STS  specify group id & artifact id  then select maven – quickstart – archetype \
step 2 : add below specified dependency in pom.xml \
               `<parent> ` \
                       `<groupId>org.springframework.boot</groupId> ` \
                     ` <artifactId>spring-boot-starter-parent</artifactId> ` \
                     ` <version>1.5.6.RELEASE</version> ` \
             ` </parent> ` \
            ` <dependencies> ` \
                   ` <dependency> ` \
                            ` <groupId>org.springframework.boot</groupId> ` \
                          `  <artifactId>spring-boot-starter-web</artifactId> ` \
                  ` </dependency> ` \
           ` </dependencies> ` 

see these  “spring-boot-starter-web”  will download all the dependent jars required to run a common spring web application . \
And the  “spring-boot-starter-parent” is application given by  spring boot people itself , we are kepping it in parent because , \
if some updates will be given by spring boot people then we should automatically get the updates with its build .  \
SO our applications will always  go to “spring – boot – starter – parent “ and look for some updates , \
if there are any then it will make the build and include it in our project . \

step 3 : add a main class in source folder  \
              ` @SpringBootApplication ` \
             `  public class SpringBootApp  { ` \
                      `  public static void main(String[] args)  { ` \
                                ` SpringApplication.run(SpringBootApp.class, args); ` \
                       ` } ` \
               ` } ` 
             
###@SpringBootApplication### annotation, means this is the starting point for our Spring Boot application
or every spring boot application we have to create a main class and that need to be annotate with @SpringBootApplication and bootstrap it .  because we don’t have any DispatcherServlet  defined here , all these will be handled internally by @SpringBootApplication 
