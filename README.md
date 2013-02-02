## Mmmbot 

### Setup

Modify `./config/sys.config`.

```erlang
[ 
  {mmmbot, [{host, "<IRC HOST>"},
            {port, <IRC PORT>},
            {nickname, "mmmbot"},
            {channel, "<CHANNEL>"}]},

  {mmmbot_images, [{access_key, "<AWS KEY>"},
                   {secret_key, "<SECRET KEY>"},
                   {bucket, "<S3 BUCKET>"}]},
                   
  {lager, [
           {handlers, [
                        {lager_console_backend, info}
                      ]}
          ]}
   ]}
].

```

### Build and Run

```shell
$ make rel
$ _rel/bin/mmmbot
.......

1> mmmbot_images:start().
ok
```
