# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


# Try write site on Ruby-on-Rails on:

##  Windows
* IMPORTANT: in windows at the end it didn't work, better move to ubuntu. If you can handle it - try.

### Ruby on rails install:
* Go to https://rubyinstaller.org/downloads/
* Download latest version of 'Ruby+Devkit XXX'
* Install it. Check 'MSYS2...'
* After Ruby installed, MSYS2 opened in cmd, press ENTER
* Restart cmd, install rails: 
  * gem install rails
* Restart cmd, check version:
  * ruby -v
  * rails -v
  * bundler -v
* All of those shall return versions
* For example:
  * ruby -v
  * ruby 3.1.2p20 (2022-04-12 revision 4491bb740a) [x64-mingw-ucrt]
  * rails -v
  * Rails 7.0.3.1
  * bundler -v
  * Bundler version 2.3.7

### Ruby on rails application create:
* create directory, go inside
* in cmd: rails new webapp
* wait for finish
* install sqlite:
  * go to created folder
  * Open file: Gemfile
  * Replace line 'gem "sqlite3", "~> 1.4"' wit next:
    * gem 'sqlite3', git: "https://github.com/larskanis/sqlite3-ruby", branch: "add-gemspec"
  * Save file
  * in cmd goto directory and write: bundle install
* in cmd write: rails server

##  Ubuntu using RVM
* Check if ruby installed:
  * in cmd: ruby -v
* Check where is installed:
  * in cmd: which ruby
  * If is not installed - install it (see after)
  * if it installed in system user (which command returns: /usr/bin/ruby) - uninstall it and install it (see after)
  * if it installed in your user (which command returns: /home/[your_user_name]/.rvm/) - is ok , no need uninstall
* do update list of packets:
  * in cmd: sudo apt-get install
* install all needed packages. In cmd:
  * sudo apt-get install libgdbm-dev libncurses5-dev automake libtool bison git-core zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev software-properties-common libffi-dev
* install RVM: go to rvm.io and execute:
  * Install GPG key
  * Install RVM
* Set terminal settings: Run command as a login shell
* Check installed version of RVM: 
  * in cmd: which RVM
* to check which ruby installed in system:
  * in cmd: rvm list
  * currently no ruby installed, so it shall be empty
* to check which ruby can be installed:
  * in cmd: list rvm known
* lets install ruby version 3.0.2:
  * in cmd: rvm install 3.0.2
* check again installed. you will see version
* After installed ruby, also we have access to gem utility. It helps to install different libraries.
* Lets install debugger:
  * in cmd: gem install byebug
* To check where it installed:
  * in cmd: gem info byebug
* Install rails:
  * in cmd: gem install rails
* NodeJS installation
* Reminder of node <-> Ruby
  *          JavaScript <-> Ruby
  * Interpretator: node <-> ruby
  * package manager: npm  <-> gem
  * environment : npm, yarn etc <-> bundler
  * list of dependencies: package.json <-> Gemfile
  * dependency management: yarn.lock <-> Gemfile.lock
* Add NodeJS repository version 12:
  * in cmd: curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
* Add yarn repository:
  * in cmd: curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
  * echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
* install yarn and nodejs:
  * in cmd: sudo apt-get install nodejs yarn
* create and run app:
  * create dir
  * go inside
  * in cmd: rails new my_app
  * go inside my_app
  * to run server, in cmd: rails start

### rdp
https://docs.microsoft.com/en-us/azure/virtual-machines/linux/use-remote-desktop?tabs=azure-cli