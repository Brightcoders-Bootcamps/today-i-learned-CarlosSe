# Today I Learned by *Carlos Segura*

Ruby and Rails official documentation reading personal journal

## Week 1

### Thu 23, July 2020 *Development environment*
I read chapter 1.1 Up and running and 1.1.1 Development environment from book *Ruby on Rails Tutorial*, I learned about adventages of Rails, I like the fact that Rails doesn't change fast, I also learned how to setup development environment in Cloud9, Cloud9 is part of AWS so develompment environment will run on browser

### Fri 24, July 2020 *Installing Rails*
I learned about how to install Rails, expecifically version 6.0.3.2, Rails is installed using gem command wich is the package manager for Ruby, I also read how to make a directory for Rails project and reviewed some Unix commands

### Mon 27, July 2020 *The first application*
I learned how to create a Rails project using the command rails new *app name* I also reviewed all directories created by the command and I found some similarities with Laravel folder structure

### Tue 28, July 2020 *Bundler*
I edited the Gemfile to match the versions used in the book, I learned how works ~> and >= for fetching the versions of gems, >= notation always installs the latest gem, whereas the ~> will install the number of version given 

### Wed 29, July 2020 *rails server*
I learned how to run script to run a server and see rails app, the server runs on localhost on port 3000, I also configured Cloud9 to allow connections to local webs server.

## Week 2

### Thu 30, July 2020 *Model-View-Controller (MVC)*
I learned how Rails use MVC architectural pattern, browser sends a request and controller handles it, then render view and sent to a the browser, the model interacts whit database.

### Fri 31, July 2020 *Hello, world*
In this section I learned how to create a first controller to render Hello World, in controller I created a function called hello in class AplicationController which inherit from ActionController, inside method I write render html: "Hello world" then modify routes where I write root 'application#hello' the syntaxis is controller_name#action_name

### Mon 03, August 2020 *Version control with Git*
I read about Git installation, configuration and basic commands like init, add, status and commit

### Tue 04, August 2020 *GitHub*
I read the section 1.3.3 GitHub, I learned more about git branches and how is helpful for a single-developer, also learned the path to work with branches until merge

### Wed 05, August 2020 *Heroku setup and deployment*
I had never used heroku, Heroku uses PostgreSQL database, is necessary to add this gem to Rails env and also modify the Gemfile, for deploying to heroku only run git push heroku master

### Thu 06, August 2020 *A toy app*
I learned about Scaffolding function, this function allow create quick and easy code, relies on command generate code by Rails, this command generate a basic structure of project (Controller, model, views, routes and migrations), I also learned how to undo a scaffold with command rails d scaffold [name of scaffold] but also is recommend generate all files manually or delete no used generated code.

### Fri 07, August 2020 *Scaffolding*
Rails scaffolding generates routes for listing elements, in tutorial the example are users, index list all users, show page shows user with id given, new allow to create a new user and save it on database, and edit allow modify registered data.

### Mon 10, August 2020 *MVC in action*
I learned how MVC works in Rails, the first step is when user request a URL, then rails routes the action in controller, the controller look to retrive information from model, the model returns a list to controller, the controller saves the list in variable, this variable is passed to view, the view render page as HTML.

### Tue 11, August 2020 *REST*
I learned about REST,  is an acronym for REpresentational State Transfer, REST are modeled as resources that can be created, read, updated, and deleted and are requested by the HTTP methods POST, GET, PATCH and DELETE this helps to make choices about which controllers and actions to write

### Wed 12, August 2020 *Weaknesses of scaffolding*
Use scaffold has a severe waknesses for example, Models no validate data,does not have authentication methods fot that reason allow any user perform operations, scaffolding includes basic test but important tests are for data validation, all views does not have styles and the most important is that the code generate is mostly not understanded

### Thu 13, August 2020 *Validations*
I learned about Rails validation, the validation is realizated in models in this case the content of mircropost is limited with 
validates :content, length: { maximum: 140 }

### Fri 14, August 2020 *Associations*
Association is a connection between models the types of associations in rails are
    belongs_to
    has_one
    has_many
    has_many :through
    has_one :through
    has_and_belongs_to_many

### Mon 17, August 2020 *Has many*
Is used to set up many to many connection with model, indicates that can be matched with zero or more instances of another model, for example, in tutorial the code is:
User - has_many :microposts
Micropost - belongs_to :user

Rails console is usefful to test models and relationships

### Tue 18, August 2020 *Inheritance hierarchies*
Models are inherited from ApplicationRecord for example,
class User < ApplicationRecord
And this inherits from ActiveRecord::Base, wich is the base class for models provided by Active Record this allow to communicate with the database and treat the database columns as Ruby attributes.

Controller are inherited from ApplicationController for example,
class UserController < ApplicationController
And this inherits from ActionController::Base wich is the base class for controllers provided by Action Pack

### Wed 19, August 2020 *Static pages*
Shorcuts for commands are
rails server = rails s
rails console = rails c
rails generate = rails g
rails test = rails t
bundle install = bundle

For undo files automatically use command destroy, examples, 
rails destroy controller StaticPages home help
rails destroy model User

For undo a single migration use
rails db:rollback

To go at beginning use
rails db:migrate VERSION=0

### Thu 20, August 2020 *HTTP Operations*
Operations betweem iser amd server are
GET - Used for reading data on the web
POST - Are typically used for creating things
PATCH - Update
DELETE - Destroy

### Fri 21, August 2020 *Getting started with testing*
Benefits of automated test:
1. Test protect against regresions, where a functioning feature stops working for some reason.
2. Test allow code to be refactoresd with confidence.
3. Test act as client for the application code, determine its design and its interface with other parts of the system.

When we should test first:
- When a test is especially short or simple compared to the application code it tests, lean toward writing the test first.
- When the desired behavior isn’t yet crystal clear, lean toward writing the application code first, then write a test to codify the result.
- Because security is a top priority, err on the side of writing tests of the security model first.
- Whenever a bug is found, write a test to reproduce it and protect against regressions, then write the application code to fix it.
- Lean against writing tests for code (such as detailed HTML structure) likely to change in the future.
- Write tests before refactoring code, focusing on testing error-prone code that’s especially likely to break.
