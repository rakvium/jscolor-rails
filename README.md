# jscolor-rails

A gem that makes [JSColor](http://jscolor.com/) available to Rails applications.

## Installation

Add this line to your application's Gemfile:

    gem 'jscolor-rails'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install jscolor-rails

## Usage

Add the following to any JavaScript file:

    //= require jscolor
    
### Notes

The gem's jscolor.js is NOT the library itself. It simply requires the original jscolor file (renamed to jscolor\_vendor.js) and adds compatibility with Turbolinks and the asset pipeline.

`jscolor.dir`'s default value has been changed to `'/assets/'` because jscolor's auto-detect fails to find the images in production mode. To change the path to the asset directory, do the following in your application's JS files:

````javascript
jscolor.dir = '/path/to/assets/';
````

## Versioning

The gem version number tracks JSColor's version number.

The major, minor, and patch version numbers will always represent the JSColor version. Should a gem bug be discovered, a 4th version identifier will be added and incremented.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Changelog

* __17/12/2014 1.4.4__ Updated jscolor.js to 1.4.4
* __07/02/2013 1.4.2.1__ Support for Rails 4 asset pipeline and Turbolinks. Moved customisations out of vendor jscolor.js.
* __17/12/2013 1.4.2__ Updated jscolor.js to 1.4.2
* __21/01/2013 1.4.0.1__ Fixed image URL in production mode
* __20/12/2013 1.4.0__ Initial release
