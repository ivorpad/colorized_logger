# ColorizedLogger

ColorizedLogger is a gem that provides a customizable, colorful logging solution for Rails applications, with file and line number information.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'colorized_logger'
```

And then execute:

    $ bundle install

Or install it yourself as:

    $ gem install colorized_logger

## Usage

In your Rails application, you can use ColorizedLogger like this:

```ruby
# config/application.rb
config.logger = ActiveSupport::TaggedLogging.new(ColorizedLogger::Logger.new(Rails.root.join('log', "#{Rails.env}.log")))

# In your controllers or models
logger.print "This is a debug message", color: :yellow
logger.print "Getting all #{self.all.count} posts", "custom tag", severity: :warn
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/ivorpad/colorized_logger. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [code of conduct](https://github.com/ivorpad/colorized_logger/blob/master/CODE_OF_CONDUCT.md).

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the ColorizedLogger project's codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/ivorpad/colorized_logger/blob/master/CODE_OF_CONDUCT.md).