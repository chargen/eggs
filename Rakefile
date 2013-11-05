# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "eggs"
  gem.homepage = "http://github.com/abcbots/eggs"
  gem.license = "MIT"
  gem.summary = %Q{Eggs Scrambles and Unscrambles text and strings}
  gem.description = %Q{Eggs Scrambles and Unscrambles (Encrypts and Decrypts) text and strings, and generates random keys of any length.}
  gem.email = "davemakena@gmail.com"
  gem.authors = ["Dave Makena"]
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

require 'cucumber/rake/task'
Cucumber::Rake::Task.new(:features)

task :default => :spec

require 'yard'
YARD::Rake::YardocTask.new
