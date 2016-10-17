# Pagerduty-Slapin

This is the Pagerduty Plugin or "SLAPIN" for SLAPI Bot managed by the SLAPI Team.

## Installation & Configuration

Download a copy of this [yaml](pager.yml) or copy and paste the below to pager.yml into the config/plugins directory of your SLAPI bot.

```yaml
plugin:
  type: container
  managed: true # Choose True or False for SLAPI management
  listen_type: passive # Choose passive or active.
  messageData: true # True/False to accept the message data from who sent a message
  config:
    name: pager # Name of instance
    Image: 'slapi/pagerduty' # Enter user/repo (standard docker pull procedures), you can also pull from a private repo via domain.com/repo
    Labels: labels
    Env: # List of environment variables
      - API='API_KEY'
      - SERVICE='SERVICE_ID'
    Tty: true # Set true/false for container TTY
```

## Usage

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at <https://github.com/imperiallabs/pagerduty-slapin>.

## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).