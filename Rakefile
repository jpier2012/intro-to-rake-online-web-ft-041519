namespace :greeting do
  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end

  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
end

task :environment do
  require_relative './config/environment.rb'
end

desc 'starts console'
task :console => :environment do
  Pry.start
end

namespace :db do

  desc 'migrate the database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
