# Terra Charts Play App

This is basically the same as Terra-charts-v2 written in NodeJS except I have an enforceable type system to provide context for my entities (I suppose?).  So far I've seen an example of a play application as dividing the various concerns as follows...

* 1.) Slick layer where they write in a query-like language in order to do database access.
* 2.) Services layer that want to retrieve information from the slick "database access" layer.
* 3.) API layer that services changes in someone's user experience (add items to chart, login, logout and countless other examples).  These have been contained in a concept-centric controllers.  These can return either pages or JSON is all that really matters in a web application.
* 4.) Routes layer that provides URL access to the various APIs.

... and by doing so will provide a consistency of conerns between the various layers (so important I said it twice).  There is also a setup layer for each play application where it...

* 1.) Bootstrap the application and load up a config file
* 2.) Run migrations on the database to load up information

I like laravel, a PHP application because it provides opinion on what you should use and how to divide up your application in a much similiar way as play. I can create an application by following a similiar cook-book style creation process (through the terminal!  I love CLIs).
* Set up entities that my app is going to deal with
* Create migrations for each entity to set up database with them and persist
* Set up dummy data to test my application
* Expose pages to a front end
* Write a front end application (aka extract it from the node version of terra charts v2!)
* Create animations!