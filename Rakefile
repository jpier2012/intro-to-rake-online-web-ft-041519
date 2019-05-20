desc 'starts console'
task :console do
  Pry.start
end

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

namespace :db do
  task :environment do
    require_relative './config/environment.rb'
  end

  desc 'migrate the database'
  task :migrate => :environment do
    Student.create_table
  end
end
