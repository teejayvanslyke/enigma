require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "enigma"
    gem.summary = %Q{Key/secret authentication gem for your web services}
    gem.description = %Q{Key/secret authentication gem for your web services}
    gem.email = "teejay.vanslyke@gmail.com"
    gem.homepage = "http://github.com/teejayvanslyke/enigma"
    gem.authors = ["teejayvanslyke"]
    gem.add_development_dependency "rspec", ">= 2.0.0"
    gem.add_development_dependency 'rack-test'
    gem.add_development_dependency 'sinatra'
    gem.add_dependency 'rack'
    gem.add_dependency 'httparty'
    gem.add_dependency 'addressable'
    gem.add_dependency 'rest_client'
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

RSpec::Core::RakeTask.new(:rcov) do |spec|
  spec.pattern = 'spec/**/*_spec.rb'
  spec.rcov = true
end

task :default => :spec

require 'rdoc/task'
RDoc::Task.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "campistrano #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
