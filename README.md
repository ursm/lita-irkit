# lita-irkit

Use IRKit on Lita

## Installation

Add lita-irkit to your Lita instance's Gemfile:

``` ruby
gem "lita-irkit"
```


## Configuration

```
config.handlers.irkit.deviceid  = ENV["IRKIT_DEVICEID"]
config.handlers.irkit.clientkey = ENV["IRKIT_CLIENTKEY"]
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
