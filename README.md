# QRCode Pix Ruby

[![CI](https://github.com/pedrofurtado/qrcode_pix_ruby/actions/workflows/ci.yml/badge.svg)](https://github.com/pedrofurtado/qrcode_pix_ruby/actions/workflows/ci.yml)
[![Gem Version](https://badge.fury.io/rb/qrcode_pix_ruby.svg)](https://badge.fury.io/rb/qrcode_pix_ruby)
[![Gem](https://img.shields.io/gem/dt/qrcode_pix_ruby.svg)]()
[![license](https://img.shields.io/github/license/pedrofurtado/qrcode_pix_ruby.svg)]()

Ruby gem for Qrcode generation of Pix (Pagamento Instantâneo Brasileiro - Banco Central do Brasil)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'qrcode_pix_ruby'
```

And then execute:

    bundle install

Or install it yourself as:

    gem install qrcode_pix_ruby

## Usage

```ruby
require 'qrcode_pix_ruby'

pix = QrcodePixRuby::Payload.new

pix.pix_key        = '12345678900'
pix.description    = 'Pagamento do pedido 123456'
pix.merchant_name  = 'William Costa'
pix.merchant_city  = 'SAO PAULO'
pix.transaction_id = 'WDEV1234'
pix.amount         = '100.00'
pix.repeatable     = false

puts pix.payload
puts pix.base64
```

## Useful links

* https://github.com/joseviniciusnunes/qrcode-pix
* https://www.gerarpix.com.br
* https://github.com/fbbergamo/gerador-pix
* https://pix.ae
* https://pix.nascent.com.br/tools/pix-qr-decoder
* https://openpix.com.br/qrcode/scanner
* https://openpix.com.br/qrcode/debug
* https://github.com/william-costa/wdev-qrcode-pix-estatico-php
* https://www.youtube.com/watch?v=eO11iFgrdCA

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/pedrofurtado/qrcode_pix_ruby. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [code of conduct](https://github.com/pedrofurtado/qrcode_pix_ruby/blob/master/CODE_OF_CONDUCT.md).

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the qrcode_pix_ruby project's codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/pedrofurtado/qrcode_pix_ruby/blob/master/CODE_OF_CONDUCT.md).
