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