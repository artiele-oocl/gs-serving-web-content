# gs-serving-web-content

**Controller: GreetingController**
This is a controller as identified by the @Controller which handles HTTP requests.
In our example, @GetMapping handles GET request of "/greeting". The controller method greeting() may accept a query parameter
named 'name' such that '/greeting?name=ARTIELE' with default value "World" if 'name' is not specified. The query parameter
binds its value on greeting() parameter name by using @RequestParam.
This controller returns a View greeting.html. In order for this view to access the query parameter passed into greeting(),
its value is added to Model object model using addAttribute().

**View: greeting.html**
This is the View that is returned by method from GreetingController.greeting(). You added the value of name in Model object
before rendering the view greeting; the value can be accessed by ${attribute_name} using Thymeleaf.
As seen in greeting.html, Thymeleaf is assigned namespace 'th' so you could use it in your View.

**Lauch: Application**
To launch the application, just add the annotation @SpringBootApplication which is a shorthand for @Configuration, @EnableAutoConfiguration,
and @ComponentScan. The Spring Boots method SpringApplication.run() is used to launch the whole applciation

**Test: ApplicationTest**
This holds the tests cases for testing the features of the application:
- Testing the homepage : homePage()
- Testing the greeting without query parameters : greeting()
- Testing the greeting with query parameter : greetingWithUser()

