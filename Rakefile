#require 'rake/testtask'
require 'rake/rdoctask'
require 'rake/contrib/sshpublisher'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |s|

    s.name = 'edave-enumerated_attribute'
    s.platform = Gem::Platform::RUBY
    s.description = 'Enumerated model attributes and view helpers'
    s.summary = 'Add enumerated attributes to your models and expose them in drop-down lists in your views'

    s.add_dependency('meta_programming', '>= 0.2.1')

    exclude_folders = 'spec/rails/{doc,lib,log,nbproject,tmp,vendor,test}'
    exclude_files = FileList['**/*.log'] + FileList[exclude_folders+'/**/*'] + FileList[exclude_folders]
    s.files = FileList['{examples,lib,tasks,spec}/**/*'] + %w(CHANGELOG.rdoc init.rb LICENSE Rakefile README.rdoc .gitignore) - exclude_files
    s.require_path = 'lib'
    s.has_rdoc = true
    s.test_files = Dir['spec/*_spec.rb']

    s.author = 'Jeff Patmon'
    s.email = 'jpatmon@gmail.com'
    s.homepage = 'http://github.com/jeffp/enumerated_attribute/tree/master'
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler not available. Install it with: gem install jeweler"
end