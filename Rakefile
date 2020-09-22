require 'html-proofer'
require 'rake'
include FileUtils

desc 'run htmlproofer, rspec if exists'
task :test do
  opts = {
    :check_external_hash => true,
    :allow_hash_href => true,
    :disable_external => true,
    :empty_alt_ignore => true,
    :only_4xx => true,
    :verbose => true
  }
  HTMLProofer.check_directory('./_site', opts).run
  sh 'bundle exec rspec' if File.exist?('.rspec')
end
