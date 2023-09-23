desc 'allows enviroment file access'
task :environment do
  require_relative './config/environment'
end 

namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola from Rake"
  end
end

namespace :db do
  desc 'migrate changes to database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with dummy data'
  task :seed do 
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end


