require_relative './config/environment'
require 'sinatra/activerecord/rake'

desc "Runs a Pry console"
task :console do
  # This line turns on logging of the SQL generated by Active Record
  ActiveRecord::Base.logger = Logger.new(STDOUT)
  
  # Open a Pry session
  Pry.start
end

desc "Start the server"
task :server do
  exec "rerun -b 'rackup config.ru'"
end 
