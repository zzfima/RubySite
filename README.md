# RubySite
Try write site on Ruby-on-Rails

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
* 