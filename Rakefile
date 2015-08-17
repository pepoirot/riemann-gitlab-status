require 'rubygems'
require 'rubygems/package_task'
require 'rdoc/task'
require 'find'

# Don't include resource forks in tarballs on Mac OS X.
ENV['COPY_EXTENDED_ATTRIBUTES_DISABLE'] = 'true'
ENV['COPYFILE_DISABLE'] = 'true'

# Gemspec
gemspec = Gem::Specification.new do |s|
  s.rubyforge_project = 'riemann-gitlab-status'

  s.name        = 'riemann-gitlab-status'
  s.version     = '0.0.1'
  s.authors     = ['Pierre-Etienne Poirot']
  s.email       = 'pepoirot@gmx.com'
  s.description = 'Extension of riemann-tool to monitor the status of a Gitlab instance'
  s.homepage    = 'https://github.com/pepoirot/riemann-gitlab-status'
  s.license     = 'LICENSE'
  s.platform    = Gem::Platform::RUBY
  s.summary     = 'riemann-gitlab-status'
  s.files       = ['bin/riemann-gitlab-status']

  s.add_runtime_dependency 'riemann-tools', '~> 0.2', '>= 0.2.6'
  s.required_ruby_version = '>= 1.8.7'

  s.executables |= Dir.entries('bin/')
  s.files = FileList['lib/**/*', 'bin/*', 'LICENSE', 'README.markdown'].to_a
  s.has_rdoc = true
end

Gem::PackageTask.new gemspec do |p|
end

RDoc::Task.new do |rd|
  rd.main = 'Riemann Gitlab Status'
  rd.title = 'Riemann Gitlab Status'
  rd.rdoc_dir = 'doc'
end
