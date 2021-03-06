# Jekyll::Amazon

Liquid tag for display Amazon Associate Links in Jekyll sites: `{% amazon %}`.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'jekyll-amazon'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install jekyll-amazon

And set the environment variables required by the Product Advertising API:

    $ export ECS_ASSOCIATE_TAG=...
    $ export AWS_ACCESS_KEY_ID=...
    $ export AWS_SECRET_KEY=...

(`ECS_ASSOCIATE_TAG` is the Tracking ID for your Affiliate account; `AWS_ACCESS_KEY_ID` and `AWS_SECRET_KEY` are your security credentials from your AWS account.  An AWS account is required for the use of this API.)

Finally, add the following to your site's `_config.yml`:

```
gems:
 - jekyll-amazon
```

## Configuration

Put the configuration in your _config.yml:

```
jekyll-amazon:
  locale: 'ja'  # label's language. default: 'en'
  country: 'jp' # with the two character country code of their Amazon
                # Affiliate account (e.g. `'us'` for United States).
                # default: 'us'
                # 'br'/'ca'/'cn'/'de'/'es'/'fr'/'in'/'it'/'jp'/'mx/'uk'/'us'
  template_dir: '_templates' # original template directory
```


## Usage

Use the tag as follows in your jekyll pages, posts and collections:

```liquid
{% amazon 4083210443 detail %}
```


## References

- [Amazon Product Advertising API](https://affiliate-program.amazon.com/gp/advertising/api/detail/main.html).
- [jugend/amazon\-ecs: Ruby Amazon Product Advertising API](https://github.com/jugend/amazon-ecs)

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/tokzk/jekyll-amazon.

