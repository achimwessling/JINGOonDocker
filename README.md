# JINGOonDocker

This image makes [Jingo](https://github.com/claudioc/jingo) available on Docker.
The image is based upon alpine, this way it's really small.

Details of this nice wiki solution can be found on its homepage [https://github.com/claudioc/jingo](https://github.com/claudioc/jingo).

## Usage
Data and configuration file are stored under the *volume* `/app/data`. So an  installation
under docker can be as easy as this:

```
> docker run -d -v "/opt/docker/volumes/jingo:/app/data" -p 6067:6067 --restart always --name jingo 33wessling824/jingoondocker
```

After this you could get the starting page at [http://localhost:6067](http://localhost:6067),
but it isn't possible to login! Following the above example you have to configure
a valid login method in the file `/opt/docker/volumes/jingo/conf/config.yaml` and
restart the image.
