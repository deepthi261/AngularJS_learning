# AngularJS_learning

On a high level, AngularJS is a framework that binds your HTML (views) to JavaScript objects (models). When your models change, the page updates automatically. The opposite is also true – a model, associated with a text field, is updated when the content of the field is changed. Angular handles all the glue code, so you don’t have to update HTML manually or listen for events, like you do with jQuery. As a matter of fact, none of the examples here even include jQuery!

To use AngularJS, you have to include it in your page before the closing <body> tag. Google’s CDN is recommended for a faster load time:

<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.0.7/angular.min.js"></script>

AngularJS gives you a large number of directives that let you associate HTML elements to models. They are attributes that start with ng- and can be added to any element. The most important attribute that you have to include in any page, if you wish to use Angular, is ng-app:

<body ng-app>

It should be added to an element that encloses the rest of the page, like the body element or an outermost div. Angular looks for it when the page loads and automatically evaluates all directives it sees on its child elements.

Here is my few examples:

 Navigation Menu

As a first example, we will build a navigation menu that highlights the selected entry. The example uses only Angular’s directives, and is the simplest app possible using the framework. Click the “Edit” button to see the source code.

 Inline Editor

For the second example, we will create a simple inline editor – clicking a paragraph will show a tooltip with a text field. We will use a controller that will initialize the models and declare two methods for toggling the visibility of the tooltip. Controllers are regular JavaScript functions which are executed automatically by Angular, and which are associated with your page using the ng-controller directive:

 Order Form

In this example, we will code an order form with a total price updated in real time, using another one of Angular’s useful features – filters. Filters let you modify models and can be chained together using the pipe character |. In the example below, I am using the currency filter, to turn a number into a properly formatted price, complete with a dollar sign and cents. You can easily make your own filters, as you will see in next example.

 Instant Search

This example will allow users to filter a list of items by typing into a text field. This is another place where Angular shines, and is the perfect use case for writing a custom filter. To do this though, we first have to turn our application into a module.

 Switchable Grid

Another popular UI interaction is switching between different layout modes (grid or list) with a click of a button. This is very easy to do in Angular. In addition, I will introduce another important concept – Services. They are objects that can be used by your application to communicate with a server, an API, or another data source. In our case, we will write a service that communicates with Instagram’s API and returns an array with the most popular photos at the moment.
