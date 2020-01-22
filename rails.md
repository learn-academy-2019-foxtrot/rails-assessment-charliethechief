# ASSESSMENT 5: INTRO TO RAILS
## Interview Practice Questions

Answer the following questions. First, without external resources. Challenge yourself to answer from memory. Then, research the question to expand on your answer. Even if you feel you have answered the question completely on your own there is always something more to learn.

1. MVC (Model View Controller) is a pattern for the architecture of a software program. Give a brief description of each component and describe how Ruby on Rails handles MVC.

  Your answer: The model is part of the ActiveRecord, View is how to data is presented, and the controller manages how the app runs.

  Researched answer:
  Model (ActiveRecord ): It maintains the relationship between the objects and the database and handles validation, association, transactions, and more.

  View ( ActionView ):It is a presentation of data in a particular format, triggered by a controller's decision to present the data. They are script-based template systems like JSP, ASP, PHP, and very easy to integrate with AJAX technology.

  Controller ( ActionController ): The facility within the application that directs traffic, on the one hand, querying the models for specific data, and on the other hand, organizing that data (searching, sorting, messaging it) into a form that fits the needs of a given view.



2. Using the information given, fill in the blanks to complete the steps for creating a new view in a Rails application.

  Step 1: Create the "route" in the file config/routes.rb
  ```
  get '/about' => 'statics#about'
  ```

  Step 2: Create the __controller.rb__ in the file __app/controllers__
  ```
  class __App__ < ApplicationController
    def __index__
    __app__ = __App.all__
      render --json: app__
    end
  end
  ```

  Step 3: Create the View in the file __app/views/index.html.erb__
  code:
  ```
  <div>This is the About page!</div>
  ```


3a. Consider the Rails routes below. Describe the responsibility of  each route.


/users/       method="GET"     # :controller => 'users', :action => 'index'
Shows all users.

/users/1      method="GET"     # :controller => 'users', :action => 'show'
Shows a user with the id of 1.

/users/new    method="GET"     # :controller => 'users', :action => 'new'
Gets the form to create a new user.

/users/       method="POST"    # :controller => 'users', :action => 'create'
Creates a new user.

/users/1/edit method="GET"     # :controller => 'users', :action => 'edit'
Gets the form the edit a user.

/users/1      method="PUT"     # :controller => 'users', :action => 'update'
Puts the ability to update a user.

/users/1      method="DELETE"  # :controller => 'users', :action => 'destroy'
Deletes a user.

3b. Which of the above routes must always be passed params and why?

answer: Post must always be passed parems because it needs to make sure whatever is being posted must meet the requirements.

4. What is the public folder used for in Rails?

  Your answer: To make things show up and change the styles as well.

  Researched answer:  Like the public directory for a web server, this directory has web files that don't change, such as JavaScript files (public/javascripts), graphics (public/images), stylesheets (public/stylesheets), and HTML files (public).



5. Write a rails route for a controller called "main" and a page called "game" that takes in a parameter called "guess"

 'main.controller.rb' => 'game'
 /users/       method="GET"     # :controller => 'users', :action => 'index'

6. In an html form, what does the "action" attribute tell you about the form? How do you designate the HTTP verb for the form?

  Your answer: It tells the form what it needs to do. You decide which verb to use depending on which CRUD action needs to be fulfilled.

  Researched answer: The action attribute specifies where to send the form-data when a form is submitted. The acronym CRUD stands for create, read, update and delete. These are the four basic functions of persistent storage. Also, each letter in the acronym can refer to all functions executed in relational database applications and mapped to a standard HTTP method, SQL statement or DDS operation.



7. Name two rails generator commands and what files they create:

  Your answer:
  rails db:create = this will create a database that can be used.
  rails generate = this can be used to create many different things

  Researched answer:
rails console
rails server
rails test
rails generate
rails db:migrate
rails db:create
rails routes
rails dbconsole
rails new app_name



8. Rails has a great community and lots of free tutorials to help you learn. Choose one of these resources and look through the material for 10-15 min. List three new things you learned about Rails:
- [Ruby on Rails Tutorial](https://www.tutorialspoint.com/ruby-on-rails/index.htm)
- [Rails for Zombies](http://railsforzombies.org)
- [Rails Guides](http://guides.rubyonrails.org/getting_started.html)

1. Convention Over Configuration: Rails has opinions about the best way to do many things in a web application, and defaults to this set of conventions, rather than require that you specify minutiae through endless configuration files.

2. Purpose of rails router: The Rails router recognizes URLs and dispatches them to a controller's action, or to a Rack application. It can also generate paths and URLs, avoiding the need to hardcode strings in your views.



3.Route globbing is a way to specify that a particular parameter should be matched to all the remaining parts of a route. For example:

9. STRETCH: What are cookies? What is the difference between a session and a cookie?

  Your answer:

  Researched answer:
