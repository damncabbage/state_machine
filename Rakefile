require 'rubygems'
require 'bundler'
Bundler.setup

require 'rake'
require 'rake/testtask'
require 'wwtd/tasks'

desc 'Default: run all tests via Travis-CI simulation.'
task :default => 'wwtd:local'

desc "Test state_machine."
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.test_files = Dir["test/{functional,unit}/**/*_test.rb"]
  t.verbose = true
  t.warning = true if ENV['WARNINGS']
end

load File.dirname(__FILE__) + '/lib/tasks/state_machine.rake'
