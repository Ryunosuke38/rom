require "rspec/core/rake_task"
require "rubocop/rake_task"

RSpec::Core::RakeTask.new(:spec)

require 'rubocop' rescue LoadError

if defined?(RuboCop)
  task default: [:spec, :rubocop]

  RuboCop::RakeTask.new do |task|
    task.options << "--display-cop-names"
  end
else
  task default: [:spec, :rubocop]
end
