# lita-irkit

Use IRKit on Lita

## Installation

Add lita-irkit to your Lita instance's Gemfile:

``` ruby
gem "lita-irkit"
```


## Configuration

```
def self.default_config(handler_config)
  handler_config.deviceid  = ENV['IRKIT_DEVICEID']
  handler_config.clientkey = ENV['IRKIT_CLIENTKEY']
end
```

## Usage

```
route /^ir list/,        :ir_list,   command: true, help: { "ir list"                  => "list irkit command names" }
route /^ir save (.+)/,   :ir_save,   command: true, help: { "ir save [command_name]"   => "save irkit command as name" }
route /^ir send (.+)/,   :ir_send,   command: true, help: { "ir send [command_name]"   => "send irkit command" }
route /^ir remove (.+)/, :ir_remove, command: true, help: { "ir remove [command_name]" => "remove irkit command" }
```

## License

[MIT](http://opensource.org/licenses/MIT)
