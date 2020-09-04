namespace :greeting do
desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

console do
  desc 'drop into the Pry console'
  task :console => :environment do
    require_relative './config/environment'
  end
    Pry.start
  end
end

namespace :db do
  desc 'migrate changes to your database'
  task :environment do
    require_relative './config/environment'
  end
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with some yummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
