# Software Architecture Patterns

p.56, [Pro ASP.NET Core MVC 2 Seventh Edition](https://www.apress.com/gp/book/9781484231494) 


&nbsp;
## Smart UI Pattern 

common in Windows Forms or ASP.NET Web Forms apps

![](smartui.png?raw=true)

* ideal for simple projects because you can get some good results quickly
* difficult to maintain and extend


&nbsp;
## Model-View Architecture

pulls out the business logic into a separate domain model

![](mv.png?raw=true)

* improvement over the monolithic smart UI pattern, much
easier to maintain
* difficult to perform unit testing on either the UI or the domain model
* contains a mass of data access code so the data model does not contain just the business data, operations, and rules.


&nbsp;
## Classic Three-Tier Architecture

separates the persistence code from the domain model and places it in a new component called the data access layer (DAL)

![](threetier.png?raw=true)

* most widely used pattern for business applications
* no constraints on how the UI is implemented
* good separation of concerns without being too complicated
* lack of enforced discipline may lead to thinly disguised smart UI applications, with no real separation of concerns



&nbsp;
## [The MVC Pattern](The MVC Pattern.md)


&nbsp;
## Variations on MVC

### Model-View-Presenter Pattern

designed to fit more easily with stateful GUI platforms such as Windows Forms or ASP.NET Web Forms

* the presenter has the same responsibilities as an MVC controller, but it also takes a more direct relationship to a stateful view, directly managing the values displayed in the UI components according
to the user’s inputs and actions
* in the *passive view implementation* the view contains no logic. The view is a container for UI controls that are directly manipulated by the presenter
* in the *supervising controller implementation* the view may be responsible for some elements of presentation logic, such as data binding, and has been given a reference to a data source from the domain models

### Model-View-View Model Pattern

a recent variation on MVC, originated from Microsoft and used in the Windows Presentation Foundation (WPF)

* models and views have the same roles as they do in MVC, but the difference is the MVVM concept of a view model, which is an abstract
representation of a user interface
* an MVVM view model has no notion that a view (or any specific UI technology) exists
* an MVVM view uses the WPF binding feature to bidirectionally associate properties exposed by controls in the view (items in a drop-down menu or the effect of pressing a button) with the properties exposed by the view model

*the MVC pattern also uses the term view model but refers to a simple model class that is used only to pass data from a controller to a view, as opposed to domain models, which are sophisticated representations of data, operations, and rules* 



