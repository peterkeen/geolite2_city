# GeoLite2 City

Includes the free [GeoLite2](https://dev.maxmind.com/geoip/geoip2/geolite2/) database from MaxMind, for a convenient way of including it in projects without having to embed a big file in your app repo or to keep it outside the repo.

MaxMind updates the database monthly on their site. We make no guarantees about updating this lib regularly, but contributions are welcome – feel free to make a pull request if you'd like us to update this gem and we haven't, or let us know if you would like to be a maintainer.

The version scheme for this gem reflects the date of the embedded MaxMind database, e.g. version `2018.08.07`. We may add another position for any maintenance releases, e.g. `2018.08.07.1`.


## Usage

`Geolite2City::DB_PATH` will be the path to the `.mmdb` database.

We recommend using it with the [MaxMindDB](https://github.com/yhirose/maxminddb) gem, e.g.

``` ruby
db = MaxMindDB.new(GeoLite2City::DB_PATH)
db.lookup("74.125.225.224")
```

See its documentation for more.


## Installation

Add this line to your application's Gemfile:

``` ruby
gem "geolite2_city"
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install geolite2_city


## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

### Updating the DB

* Download the latest from <http://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz> (linked from <https://dev.maxmind.com/geoip/geoip2/geolite2/>), unpack it and stick its contents in the `db` dir of the gem.
* Update the version of the gem to match the date in the unpacked folder name.
* Release the gem.
* Prosper‽


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

This product includes GeoLite2 data created by MaxMind, available from <http://www.maxmind.com>.
