require 'rubygems'
require 'bundler'

Bundler.setup :default, :test, :development

Bundler::GemHelper.install_tasks

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = 'spec/**/*_spec.rb'
end

task :spec

require 'rainbow/ext/string' unless String.respond_to?(:color)
require 'rubocop/rake_task'
Rubocop::RakeTask.new(:rubocop)

task default: [:rubocop, :spec]
