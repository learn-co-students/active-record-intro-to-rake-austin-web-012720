namespace :greeting do
  desc "outputs hello to the termina"
  task :hello do
    puts "hello from Rake!"
  end

  desc "outputs hola to the terminal"
    task :hola do
    puts "hola de Rake!"
  end
end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'invokes the :environment task as a dependancy'
  task migrate: :environment do
    Student.create_table
  end 

  desc 'seeds db with test data'
  task :seed do
    require_relative './db/seeds.rb'
  end 
end 

desc 'require pry'
task console: :environment do
  Pry.start
end 