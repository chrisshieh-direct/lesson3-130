require 'rake/testtask'
require 'find'

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Default task'
task :default => [:test]

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'list all files'
task :list_files do
  Find.find(Dir.pwd) do |path|
    next if path.include?("/.")
    puts path if File.file?(path)
  end
end
