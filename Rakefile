task :environment do
  require_relative './config/environment'
end

namespace :greeting do
  desc 'puts hello to terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc ':hello, but in spanish'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrate changes to database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with test data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end