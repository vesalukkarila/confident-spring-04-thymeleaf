# confident-spring-04-thymeleaf
This repository is related to module 4 in Marco Behler's course "The confident Spring professional" https://www.marcobehler.com/ which I purchased in order to understand the fundamentals of Spring. The course starts with plain Java backend and introduces plain Spring features little by little, showcasing what Spring Boot hides under the hood. At the end of the course Spring Boot features are implemented.

## Learning goals

- Rendering HTML with WebMVC
- Working with templating library Thymeleaf
- Form submissions

## Key takeaways

@Controller class, without additional annotations, serves html.    
For Thymeleaf and Spring to work together register following three @Beans:  
- ThymeLeafViewResolver; Tells Spring it should try to find Thymeleaf templates  
- SpringTemplateEngine; Thymeleaf-specific configuration bean, hooks up Spring MVC and Thymeleaf  
- SpringResourceTemplateResolver; Class that actually finds your Thymeleaf template

Through Model (essentially a map-container) you provide variables to the template.  
Spring injects Model into every @Controller method if specified as parameter.  
Thymeleaf tags have lots of code-like functionalities.  

## Getting Started

To run the application, you have two choices:
1. Run locally
2. Run in Docker

### Locally

1. Ensure all the dependencies are installed
2. Clone the repository  
3. Build the project using Maven: 
    ```sh
    mvn clean install
    ```
4. Run the application with: 
    ```sh
    java -jar target/pdfinvoices-1.0-SNAPSHOT.jar
    ```

### Run in Docker
1. Build the image:
    ```shell
    docker build . -t confident-04:latest     
    ```
2. Run the image:
    ```shell
    docker run -it -p 8080:8080 confident-04:latest 
    ```
3. Open the api in http://localhost:8080

## Documentation
Endpoints for local use:
- GET "/" optionally "/?username=jeff"
- GET "/login"
- POST "login"

  
