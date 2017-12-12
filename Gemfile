# -*- ruby -*-

source 'https://rubygems.org'

gem "airbrake", require: false # exception notifier
gem "acts_as_paranoid", "0.5.0.beta1"
# We need this until https://github.com/mbleigh/acts-as-taggable-on/issues/649
# will not be closed
gem "acts-as-taggable-on", git: 'https://git.assembla.com/acts-as-taggable-on.git'
gem 'acts_as_tree'
gem 'ar-octopus', '~> 0.8.5' #database replication(master-slaves) handler
gem 'centrifuge' #real-time
gem "configatron" # yml configuration for the app
gem "dalli" # memcache client
gem "json"
gem "kgio", "2.9.3" # used to boost dalli
gem "mysql2"
gem "rake", require: false
gem 'rails', '4.2.7.1'
gem "redis", require: false # Needed for bandit/real-time
gem 'responders', '~> 2.0'
gem "sshkey", require: false
gem "yajl-ruby", require: "yajl/json_gem"

# This is what is not loaded in main app
group :secondary do
  # Rails A/B testing.
  gem "actionpack-xml_parser" # Rails 4.0 Remove support for parsing XML parameters from request.
  gem "activemerchant" # payments gateways
  gem "acts_as_versioned", :git => "https://github.com/technoweenie/acts_as_versioned.git"
  gem "amqp" # rabbitmq client
  gem "bandit" # Rails A/B testing
  gem "bertrpc", :git => "https://git.assembla.com/bertrpc.git", :branch => :master
  gem "braintree" # payment gateway
  gem "breakout-magic-mimes", git: 'https://git.assembla.com/breakout-magic-mimes.git', branch: :master
  gem "breakout_parser", git: 'https://git.assembla.com/assembla-oss.parser.git', branch: :master
  gem 'chargify_api_ares'
  gem 'chargify2'
  gem 'countries', require: 'countries/global'
  gem "rchardet" # rchardet is an encoding auto-detection library in Ruby.
  gem "fast_xs" # provides C extensions for escaping text
  gem 'geocoder'
  gem 'github'
  gem 'google-api-client', require: 'google/api_client' # Needed for Google+ Sign-in
  gem "hashie", '~> 3.3' # compatible with github_api
  gem "htmlentities"
  gem "i18n-js", git: 'https://github.com/fnando/i18n-js.git', tag: 'v2.1.2'
  gem "icalendar", require: false
  gem "iniparse", require: false
  gem "kaminari"
  gem "magic"
  gem "mini_magick"
  gem "mime-types"
  gem 'msgpack-rpc', '0.5.4' # for wiki git backend communication
  gem "multipass", require: false # used for Desk.com integration
  gem "nokogiri", '~> 1.6.3', require: false # compatible with github_api
  gem 'prototype-rails', github: 'rails/prototype-rails', branch: '4.2'
  gem 'oauth'
  gem "oauth2"
  gem 'offsite_payments' # Needed for activemerchant integrations
  gem "rack-oauth2"
  gem "rack-openid", "~> 1.3.1", :require => "rack/openid"
  gem "rails_autolink", '1.1.5'
  gem 'rails-deprecated_sanitizer'
  gem "rbnacl-libsodium" # encryption
  gem "rdiscount"
  gem 'react-rails', '~> 1.7', '>= 1.7.1'
  gem "recaptcha", :require => "recaptcha/rails"
  gem "RedCloth"
  gem "right_aws" , git: "https://github.com/rightscale/right_aws.git", branch: :master
  gem "ruby-openid", '2.5.0', :require => "openid"
  gem "ruby-openid-apps-discovery"
  gem "ruby-saml", "0.8.1"
  gem "restforce"
  gem 'signet' # Needed for Google+ Sign-in
  gem 'slack-api', require: 'slack'
  gem "sqlite3", "1.3.10", require: false
  gem "validate_url", "0.2.0" # doc https://github.com/perfectline/validates_url
  gem "wicked_pdf"
  gem "xml-simple"
  gem "ya2yaml"
  gem "zipruby", require: false
  # kill -CONT <pid> to dump debug info into /tmp/sigdump-PID.log
  gem 'sigdump', :require => 'sigdump/setup'
  gem "premailer-rails", "1.8.0"
  gem 'aws-sdk'

  # Gems for old elasticsearch (0.20.6)
  gem "tire", :git => "https://git.assembla.com/tire.git", :branch => :rackless # use our fork until we migrate to ruby 1.9.x

  # Gem for detect mobile requests
  gem "mobile_fu-rails3"

  # material path pattern
  gem "arboreal", github: "assembla/arboreal"

  gem 'github_connector', path: 'lib/engines/github_connector'
  gem 'git_connector', path: 'lib/engines/git_connector'
  gem 'files_connector', path: 'lib/engines/files_connector'
  gem 'dropbox_connector', path: 'lib/engines/dropbox_connector'
  gem 'box_connector', path: 'lib/engines/box_connector'
  gem 'gdrive_connector', path: 'lib/engines/gdrive_connector'

  gem 'breakout_elasticsearch', path: 'lib/engines/breakout_elasticsearch', require: nil
  gem 'elastic-schema', git: 'https://github.com/leandro/elastic-schema', require: nil

  gem 'hints_suggester', path: 'lib/engines/hints_suggester', require: nil

  # Assets
  gem 'sass-rails',   '~> 4.0.0'
  gem 'coffee-rails', '~> 4.0.0'
  gem 'uglifier', '>= 1.3.0'
  gem 'jquery-rails'

  gem "messengerjs-rails", "~> 1.4.1"
  gem "zeroclipboard-rails"
  gem 'non-stupid-digest-assets'
end

group :development, :test do
  gem "byebug"
  gem "rspec-core", "~> 2.14", require: false
  gem "rspec-rails", "~> 2.14", require: false
  gem 'rspec-activemodel-mocks', require: false
  gem "ci_reporter", require: false
  gem "jasmine", "2.1.0"
  gem 'guard', '~> 2.1', require: false
  gem 'guard-coffeescript', '~> 2.0', require: false
  gem "parallel_tests", :git => "https://git.assembla.com/parallel_tests.git", :branch => :master, require: false
end

group :development do
  gem "active_record_query_trace"
  gem "rails-dev-boost", git: 'https://github.com/thedarkone/rails-dev-boost', branch: :master
  gem "ruby-prof", require: false
  gem "annotate", require: false #bundle exec annotate -mi --position before
  gem "capistrano", "2.9.0", require: false #Do not go above 2.9.0, it will not work with our cap scripts
  gem 'quiet_assets'
end

group :test do
  gem "test-unit", "3.0.9"
  # Do not require it because cruise control can not run migrations on clean db
  gem "factory_girl_rails", "~> 1.7.0", require: false
  gem "webrat"
  gem "fakeweb", require: false
  gem "database_cleaner"
  gem "codeclimate-test-reporter", require: false
  gem "thin"
end

group :production do
  gem "newrelic_rpm"
end

group :private_install do
  gem "tzinfo"
  gem "ruby-ldap"
  gem 'breakout_console', path: 'vendor/engines/breakout_console'
end

group :development, :test, :private_install do
  gem "unicorn-rails"
end

group :profile do
  gem 'benchmark-ips'
  gem 'stackprof'
  gem 'rack-mini-profiler'
  gem 'memory_profiler'
  gem 'flamegraph'
end
