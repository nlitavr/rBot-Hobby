# README

This is an Rails Application, let's call it StudentHelper for now.. set out to simplify life for the average student.

## By [rBot](http://rbotovich.herokuapp.com.br/).

This is an Rails Application, let's call it StudentHelper for now.. set out to simplify life for the average student.

## Ruby on Rails Info

* Ruby 2.1.2
* Rails 4.1.4

## Database
* [PostgreSQL 9.3.2]

## Development
* Front-End framwork Twitter-Bootstrap (Sass)
* Template engine: HAML (helpful gem/script: [html2haml](https://github.com/haml/html2haml))
 ```console
 find . -name \*.erb -print | sed 'p;s/.erb$/.haml/' | xargs -n2 html2haml
 ```
* Testing Framwork: Rspec/Cucumber
* Form builder: simple_form
* Users: [Devise](https://github.com/plataformatec/devise)

## Helpful Information
* [Rails Coding Guidelines](https://github.com/styleguide/ruby).
* [Parsing HTML with Nokogiri](http://ruby.bastardsbook.com/chapters/html-parsing/).
* [Sass Basics](http://sass-lang.com/guide) && [Bootstrap Customizations](http://getbootstrap.com/customize/).
* [10 Rails Console Tricks](http://rors.org/2009/12/20/10-rails-console-tricks).
* [Rails 4 PostgreSQL integration](http://yousefourabi.com/blog/2014/03/rails-postgresql/).
* [HABTM relationships in Rails 4](http://craiccomputing.blogspot.com/2013/11/habtm-relationships-in-rails-4.html).

## Problems I've ran into & Solutions
* When RVM lists a ruby version, but Rails thinks you're using a different version: [(has to do with Rails 4 'spring' gem)](http://stackoverflow.com/questions/19342044/in-ruby-your-ruby-version-is-1-9-3-but-your-gemfile-specified-2-0-0), answer #5 worked for me
* ...

## Getting Started

* Install RVM
```console
\curl -sSL https://get.rvm.io | bash
```
(on Ubuntu)
```console
sudo apt-get install curl && sudo apt-get update
\curl -sSL https://get.rvm.io | bash
source ~/.rvm/scripts/rvm
rvm requirements
```
* Install Ruby (important! install Ruby through RVM & no sudo!!!)
```console
rvm install 2.1.2
rvm use 2.1.2 --default
```
* Install Rails
```console
gem install rails --version 4.1.4
```
* Install Postgresql
 * Ubuntu
 ```console
 sudo apt-get update && sudo apt-get install postgresql postgresql-contrib
 sudo /etc/init.d/postgresql start
 ```
 if you get
 ```console
 Error: Cannot stat /var/run/postgresql
  * No PostgreSQL clusters exist; see "man pg_createcluster"
 ```
 run
 ```console
 sudo mkdir /var/run/postgresql && sudo chown [username]:[username] /var/run/postgresql
 ```

 * Create user (quite important)
 ```console
 createuser [username] ## should be your User login for the system
 psql -U [username] -h localhost [databasename] ## databasename in /[rails_project]/config/database.yml
 ALTER USER [username] WITH SUPERUSER ;
 \q
 ```
* Install Gems
```console
cd /[rails_project]/
bundle
```

## Ready to go!
```console
RAILS_ENV=development rails s
```










