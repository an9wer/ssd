## Usage

First, create a file named with `config.py`, which is a configuration file
used by mtprotoproxy.

Then use the following commands to deploy mtprotoproxy:

1.  Build a docker image of mtprotoproxy:

        sudo make

2.  After building, create a docker container of that:

        sudo make run

Every time when changing the content of `config.py`, you need to restart docker
container as follows:

    sudo make restart

**Note**: The commands above by default will create an image named with
`mtprotoproxy_image` and a container, whose name is `mtprotoproxy_container`,
seperately. If needed to change these names, add `IMAGE={name}` and
`CONTAINER={name}` arguments when running the commands above.

