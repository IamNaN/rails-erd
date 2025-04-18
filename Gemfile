source "https://rubygems.org"

gemspec

if ENV["edge"]
  gem "activerecord", :github => "rails/rails"
end


group :development, :test do
  gem 'minitest', '~> 5.14.0'
end

group :development do
  gem 'mocha'
  gem "logger" # is a bundled gem since Ruby 3.4
  gem "mutex_m" # is a bundled gem since Ruby 3.4
  gem "base64" # is a bundled gem since Ruby 3.4
  gem "bigdecimal" # is a bundled gem since Ruby 3.4
  gem "drb" # is a bundled gem since Ruby 3.4
  gem "benchmark" # is a bundled gem since Ruby 3.4
  gem "rake"
  gem "yard"
  gem "ostruct"

  platforms :ruby do
    gem "activerecord", "< 7.0"
    gem "activesupport", "< 7.0"
    gem "sqlite3", '~> 1.4'
    gem "redcarpet"

    if RUBY_VERSION > "2.1.0"
      gem "test-unit" # not bundled in CRuby since 2.2.0
    end
  end

  platforms :jruby do
    gem "activerecord-jdbcsqlite3-adapter"
    gem "jruby-openssl", :require => false # Silence openssl warnings.
  end
end