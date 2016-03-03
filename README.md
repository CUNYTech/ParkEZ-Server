## Park EZ API

This is solely a REST API. The [android app][] talks to this.

We are using [PostgresSQL][] with [PostGIS extensions][] for better geospatial indexing and querying capabilities.

The query used to find the closest parking spot, and the code to add the index for fast lookup were borrowed from [this blog](http://ngauthier.com/2013/08/postgis-and-rails-a-simple-approach.html).

## Development

### Bootstrapping your development environment

Ruby is obviously needed. I recommend [rvm][] for managing ruby versions.

So that people don't have to spend time installing stuff I dockerized the
app itself.

Download [docker][] and [docker-compose][]. The choice to use docker was that it just works and is easily replicated. Only one person should need to spend time setting things up like this.

Once you have done this:

simply type:

```sh
$ docker-compose up -d
```

Then just work as you would.
[android app]: https://github.com/CUNYTech/ParkEZ-Android
[docker]: https://docs.docker.com/engine/installation/linux/ubuntulinux/
[docker-compose]: https://docs.docker.com/compose/install/
[rvm]: http://rvm.io/rvm/install
[PostgresSQL]: http://www.postgresql.org
[PostGIS extensions]: http://postgis.net/install/
