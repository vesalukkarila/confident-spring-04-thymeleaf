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

## Use
Endpoints for local use:
- GET "/" optionally "/?username=jeff"
- GET "/login"
- POST "login", korjaa kunnolliseksi rajapintadokumentaatioksi 

  
