# Netvisor
[![Gem Version](https://badge.fury.io/rb/netvisor.svg)](http://badge.fury.io/rb/netvisor)
[![Coverage Status](https://coveralls.io/repos/Eficode/netvisor/badge.png)](https://coveralls.io/r/Eficode/netvisor)
[![Build Status](https://travis-ci.org/Eficode/netvisor.svg?branch=master)](https://travis-ci.org/Eficode/netvisor)

This gem aims to be a complete implementation of the Netvisor API

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'netvisor'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install netvisor

## Usage

### Configuration

```
Netvisor.configure do |config|
  config.host = Netvisor environment host
  config.sender = Name of sender (defautls to: 'Netvisor gem')
  config.customer_id = Your customer ID
  config.partner_id = Your partner ID
  config.language = language for the API
  config.organisation_id = Your organisation ID
  config.customer_key = Customer key
  config.partner_ke = Partner key
end
```

### Implemented methods

```
client = Netvisor.new
sales_invoice = ... # create A SalesInvoice object
client.send_invoice(sales_invoice)
```

### Unimplemented methods

```
req = Netvisor::Request.new
xml_data_string = ... # Some XML data string
service_name = ... # Name of netvisor service without .nv
res = req.dispatch(foo, service_name, nil, nil)
```


## Contributing

1. Fork it ( https://github.com/Eficode/netvisor/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
