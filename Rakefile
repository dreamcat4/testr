require 'rubygems'
require 'rake'


require 'bundler'
begin
  Bundler.setup(:runtime, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end



require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.name = "testr"
  gem.summary = %Q{TODO: one-line summary of your gem}
  gem.description = %Q{TODO: longer description of your gem}
  gem.email = "dreamcat4@gmail.com"
  gem.homepage = "http://github.com/dreamcat4/testr"
  gem.authors = ["Dreamcat4"]

  # Have dependencies? Add them to Gemfile



  # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
end



require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = %Q{test/**/test_*.rb}
  test.verbose = true
end

require 'rcov/rcovtask'
Rcov::RcovTask.new do |test|
  test.libs << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end




require 'cucumber/rake/task'
Cucumber::Rake::Task.new(:features)




require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "<%= project_name %> #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end




Jeweler::GhpagesTasks.new do |ghpages|
  ghpages.doc_fmt    = "rdoc"
  ghpages.keep       = []
  ghpages.keep_all   = false
  ghpages.on_release = false
  ghpages.site_root  = false
  ghpages.map_files  = {
    "rdoc" => "",
  }
end




task :default => :test
