
namespace :greeting do
	desc 'outputs hello to the terminal'
	task :hello do
  		puts "hello from Rake!"
	end

	desc 'outputs hello in Spanish to the terminal'
	task :hola do 
		puts "hola de Rake!"
	end 
end

namespace :db do
	desc 'migrate changes to your database'
	task :migrate => :environment do 
		Student.create_table
	end 

	task :environment do 
		require_relative './config/environment'
	end

	desc 'seed the database'
	task :seed do 
		require_relative './db/seeds.rb'
	end
end 

desc 'start pry'
task :console => "db:environment" do
	Pry.start
end

	

