## Usage

First, create a file named with `config.json`, which is a configuration file
used by shadowsocks (see [basic configuration][0] and [multiple user
configuration][1] about how, you can also find an example in
`config.json.example`).

Then use the following command to deploy shadowsocks:

1.  Build a docker image of shadowsocks:

        sudo make

2.  After building, create a docker container of that:

        sudo make run

That's all.

Every time change the content of `config.json`, you need to restart docker
container as follows:

    sudo make restart

**Note**: The commands above will by default create a image named with
`shadowsocks_image` and a container whose name is `shadowsocks_container`
seperately. If need to change these names, add `IMAGE={name}` and
`CONTAINER={name}` arguments when running the commands above.

[0]: https://github.com/shadowsocks/shadowsocks/wiki/Configuration-via-Config-File
[1]: https://github.com/shadowsocks/shadowsocks/wiki/Configure-Multiple-Users
