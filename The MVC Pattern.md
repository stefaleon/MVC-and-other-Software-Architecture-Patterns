# The MVC Pattern

p.53, [Pro ASP.NET Core MVC 2 Seventh Edition](https://www.apress.com/gp/book/9781484231494) 


The term model-view-controller has been in use since the late 1970s and arose from the Smalltalk project at Xerox PARC, where it was conceived as a way to organize some early GUI applications. 


An MVC application will be split into at least three pieces

* Models, which contain or represent the data that users work with
* Views, which are used to render some part of the model as a user interface
* Controllers, which process incoming requests, perform operations on the model, and select views to render to the user


&nbsp;
## The ASP.NET Implementation of MVC

In ASP.NET Core MVC, controllers are C# classes, usually derived from the Microsoft.AspNetCore.Mvc.Controller class. Each public method in a class derived from Controller is an action method, which is associated with a URL. When a request is sent to the URL associated with an action method, the statements in that action method are executed in order to perform some operation on the domain model and then to select a view to display to the client. 

![](mvc.png?raw=true)

* uses a view engine, known as Razor, which is the component responsible for processing a view in order to generate a response for the browser


&nbsp;
### [Software Architecture Patterns](Software Architecture Patterns.md)