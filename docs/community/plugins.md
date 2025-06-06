# Plugins

Dokku itself is built out of plugins and uses [plugn](https://github.com/dokku/plugn) for its plugin system. In essence a plugin is a collection of scripts that will be run based on naming convention.

Let's take a quick look at the current Dokku nginx plugin that's shipped with Dokku by default.

    nginx-vhosts/
    ├── plugin.toml  # plugin metadata
    ├── commands     # contains additional commands
    ├── install      # runs on Dokku installation
    └── post-deploy  # runs after an app is deployed

## Installing a plugin

[See the plugin management documentation](/docs/advanced-usage/plugin-management.md).

## Creating your own plugin

[See the full documentation](/docs/development/plugin-creation.md).

## Official Plugins

The following plugins are available and provided by Dokku maintainers.  Please file issues against their respective issue trackers.

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [Clickhouse](https://github.com/dokku/dokku-clickhouse)                                           | [dokku][]             | 0.4.0+                |
| [Copy Files to Image](https://github.com/dokku/dokku-copyfiles-to-image)                          | [dokku][]             | 0.4.0+                |
| [CouchDB](https://github.com/dokku/dokku-couchdb)                                                 | [dokku][]             | 0.4.0+                |
| [Cron Restart](https://github.com/dokku/dokku-cron-restart)                                       | [dokku][]             | 0.30.0+               |
| [Elasticsearch](https://github.com/dokku/dokku-elasticsearch)                                     | [dokku][]             | 0.4.0+                |
| [Grafana/Graphite/Statsd](https://github.com/dokku/dokku-graphite)                                | [dokku][]             | 0.4.0+                |
| [HTTP Auth](https://github.com/dokku/dokku-http-auth)                                             | [dokku][]             | 0.4.0+                |
| [Let's Encrypt](https://github.com/dokku/dokku-letsencrypt)                                       | [dokku][]             | 0.4.0+                |
| [Maintenance mode](https://github.com/dokku/dokku-maintenance)                                    | [dokku][]             | 0.4.0+                |
| [MariaDB](https://github.com/dokku/dokku-mariadb)                                                 | [dokku][]             | 0.4.0+                |
| [Meilisearch](https://github.com/dokku/dokku-meilisearch)                                         | [dokku][]             | 0.4.0+                |
| [Memcached](https://github.com/dokku/dokku-memcached)                                             | [dokku][]             | 0.4.0+                |
| [Mongo](https://github.com/dokku/dokku-mongo)                                                     | [dokku][]             | 0.4.0+                |
| [MySQL](https://github.com/dokku/dokku-mysql)                                                     | [dokku][]             | 0.4.0+                |
| [Nats](https://github.com/dokku/dokku-nats)                                                       | [dokku][]             | 0.4.0+                |
| [Omnisci](https://github.com/dokku/dokku-omnisci)                                                 | [dokku][]             | 0.4.0+                |
| [Postgres](https://github.com/dokku/dokku-postgres)                                               | [dokku][]             | 0.4.0+                |
| [Pushpin](https://github.com/dokku/dokku-pushpin)                                                 | [dokku][]             | 0.4.0+                |
| [RabbitMQ](https://github.com/dokku/dokku-rabbitmq)                                               | [dokku][]             | 0.4.0+                |
| [Redirect](https://github.com/dokku/dokku-redirect)                                               | [dokku][]             | 0.4.0+                |
| [Redis](https://github.com/dokku/dokku-redis)                                                     | [dokku][]             | 0.4.0+                |
| [Registry](https://github.com/dokku/dokku-registry)                                               | [dokku][]             | 0.12.0+               |
| [RethinkDB](https://github.com/dokku/dokku-rethinkdb)                                             | [dokku][]             | 0.4.0+                |
| [Scheduler Kubernetes](https://github.com/dokku/dokku-scheduler-kubernetes)                       | [dokku][]             | 0.4.0+                |
| [Scheduler Nomad](https://github.com/dokku/dokku-scheduler-nomad)                                 | [dokku][]             | 0.4.0+                |
| [Solr](https://github.com/dokku/dokku-solr)                                                       | [dokku][]             | 0.4.0+                |
| [SSH Hostkeys](https://github.com/cedricziel/dokku-hostkeys-plugin)                               | [dokku][]             | 0.4.0+                 |
| [Typesense](https://github.com/dokku/dokku-typesense)                                             | [dokku][]             | 0.4.0+                |

## Community plugins

> [!WARNING]
> The following plugins have been supplied by our community and may not have been tested by Dokku maintainers.

### Datastores

#### Relational

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [MariaDB](https://github.com/Kloadut/dokku-md-plugin)                                             | [kloadut][]           | 0.3.x                 |
| [MariaDB (single container)](https://github.com/ohardy/dokku-mariadb)                             | [ohardy][]            | 0.3.x                 |
| [MariaDB (single container)](https://github.com/krisrang/dokku-mariadb)                           | [krisrang][]          | 0.3.26+               |
| [PostgreSQL](https://github.com/jlachowski/dokku-pg-plugin)                                       | [jlachowski][]        | 0.3.x                 |
| [PostgreSQL (single container)](https://github.com/ohardy/dokku-psql)                             | [ohardy][]            | 0.3.x                 |
| [PostgreSQL (single container)](https://github.com/Flink/dokku-psql-single-container)             | [flink][]             | 0.3.26+               |
| [Edgedb](https://github.com/IgnisDa/dokku-edgedb)                                                 | [ignisda][]           | 0.27.0+               |

#### NewSQL

| Plugin                                                  | Author      | Compatibility |
| ------------------------------------------------------- | ----------- | ------------- |
| [Surrealdb](https://github.com/IgnisDa/dokku-surrealdb) | [ignisda][] | 0.27.0+       |

#### Caching

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [Nginx Cache](https://github.com/Aluxian/dokku-nginx-cache)                                       | [aluxian][]           | 0.5.0+                |
| [Redis (single container)](https://github.com/ohardy/dokku-redis)                                 | [ohardy][]            | 0.3.x                 |
| [Varnish](https://github.com/Zenedith/dokku-varnish-plugin)                                       | [zenedith][]          | Varnish cache between nginx and application with base configuration|

#### Queuing

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [RabbitMQ](https://github.com/jlachowski/dokku-rabbitmq-plugin)                                   | [jlachowski][]        | 0.3.x                 |
| [RabbitMQ (single container)](https://github.com/jlachowski/dokku-rabbitmq-single-plugin)         | [jlachowski][]        | 0.3.x                 |
| [ElasticMQ (SQS compatible)](https://github.com/cu12/dokku-elasticmq)                             | [cu12][]              | 0.5.0+                |
| [VerneMQ (MQTT Broker)](https://github.com/SpinifexGroup/dokku-vernemq)                           | [mrname][]            | 0.4.0+                |

#### Other

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [etcd](https://github.com/basgys/dokku-etcd)                                                      | [basgys][]            | 0.4.x                 |
| [FakeSNS](https://github.com/cu12/dokku-fake_sns)                                                 | [cu12][]              | 0.5.0+                |
| [InfluxDB](https://github.com/basgys/dokku-influxdb)                                              | [basgys][]            | 0.4.x                 |
| [RethinkDB](https://github.com/stuartpb/dokku-rethinkdb-plugin)                                   | [stuartpb][]          | 0.3.x                 |
| [Headless Chrome](https://github.com/lazyatom/dokku-chrome)                                       | [lazyatom][]          | 0.8.1+                |

### Plugins Implementing New Dokku Functionality

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [App name as env](https://github.com/cjblomqvist/dokku-app-name-env)                              | [cjblomqvist][]       | 0.3.x                 |
| [APT](https://github.com/dokku-community/dokku-apt)                                               | [dokku-community][]   | 0.18.x+               |
| [Auto Sync](https://github.com/IdeaSynthesis/dokku-autosync)<sup>1</sup>                          | [fomojola][]          | 0.8.1+                |
| [Deploy Webhook](https://github.com/IdeaSynthesis/dokku-deploy-webhook)<sup>2</sup>               | [fomojola][]          | 0.8.1+                |
| [Docker auto persist volumes](https://github.com/Flink/dokku-docker-auto-volumes)                 | [flink][]             | 0.4.0+                |
| [Docker Direct](https://github.com/dokku-community/dokku-docker-direct)                           | [josegonzalez][]      | 0.4.0+                |
| [Dokku Clone](https://github.com/crisward/dokku-clone)                                            | [crisward][]          | 0.4.0+                |
| [Dokku Copy App Config Files](https://github.com/dokku-community/dokku-supply-config)             | [josegonzalez][]      | 0.4.0+                |
| [Dokku Require](https://github.com/crisward/dokku-require)<sup>3</sup>                            | [crisward][]          | 0.4.0+                |
| [Global Certificates](https://github.com/josegonzalez/dokku-global-cert)                          | [josegonzalez][]      | 0.5.0+                |
| [Graduate (Environment Management)](https://github.com/glassechidna/dokku-graduate)               | [benjamin-dobell][]   | 0.4.0+                |
| [Host post-build command hook](https://github.com/baikunz/dokku-post-deploy-script)               | [baikunz][]           | 0.4.0+                |
| [Host pre-build command hook](https://github.com/fteychene/dokku-build-hook)                      | [fteychene][]         | 0.4.0+                |
| [Hostname](https://github.com/michaelshobbs/dokku-hostname)                                       | [michaelshobbs][]     | 0.4.0+                |
| [HTTP Auth Secure Apps](https://github.com/matto1990/dokku-secure-apps)                           | [matto1990][]         | 0.4.0+                |
| [Image Size Limit](https://github.com/Tashows/dokku-image-size-limit)                             | [Tashows][]           |                       |
| [Litestream](https://github.com/AxelTheGerman/dokku-litestream)<sup>4</sup>                       | [AxelTheGerman][]     | 0.27.0+               |
| [Monit (Health Checks)](https://github.com/mbreit/dokku-monit)                                    | [mbreit][]            | 0.8.0+                |
| [Monit](https://github.com/cjblomqvist/dokku-monit)                                               | [cjblomqvist][]       | 0.3.x                 |
| [Multicast DNS (mDNS)](https://github.com/calyhre/dokku-mdns)                                     | [calyhre][]           | 0.33.0+               |
| [Nuke Containers](https://github.com/dokku-community/dokku-nuke)                                  | [josegonzalez][]      | 0.4.0+                |
| [Proctype Filter](https://github.com/michaelshobbs/dokku-proctype-filter)                         | [michaelshobbs][]     | 0.4.0+                |
| [robots.txt](https://notabug.org/candlewaster/dokku-robots.txt)                                   | [candlewaster][]      | 0.4.x                 |
| [Tor](https://github.com/michaelshobbs/dokku-tor)                                                 | [michaelshobbs][]     | 0.4.0+                |
| [UFW](https://github.com/dokku-community/dokku-ufw)                                               | [josegonzalez][]      | 0.3.x                 |
| [User Access](https://github.com/mainto/dokku-access)                                             | [mainto][]            | 0.4.0+                |
| [User ACL](https://github.com/dokku-community/dokku-acl)                                          | [maciej łebkowski][]  | 0.4.0+                |

<sup>1</sup> Adds the ability to sync an application repo with a remote GitHub repo (useful for automated rebuilds without needing a git push from an external system

<sup>2</sup> Adds the ability to invoke a post-deploy webhook with the IP, port and app name, all with a single config:set).

<sup>3</sup> Extends app.json support to include creating volumes and creating / linking databases on push

<sup>4</sup> Adds SQLite replication to external object storage via [Litestream](https://litestream.io)

### Other Plugins

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [Chef cookbook](https://github.com/nickcharlton/dokku-cookbook)                                   | [nickcharlton][]      |                       |
| [Discourse](https://github.com/badsyntax/dokku-discourse)                                         | [badsyntax][]         | 0.21.4+               |
| [Tailscale](https://github.com/andrew-womeldorf/dokku-tailscale)                                  | [andrew-womeldorf][]  | 0.34.4+               |
| [Wordpress](https://github.com/dokku-community/dokku-wordpress)                                   | [dokku-community][]   | 0.4.0+                |

### Deprecated Plugins

The following plugins have been removed as their functionality is now in Dokku Core.

| Plugin                                                                                            | Author                | In Dokku Since                            |
| ------------------------------------------------------------------------------------------------- | --------------------- | ----------------------------------------- |
| [Airbrake deploy](https://github.com/Flink/dokku-airbrake-deploy)                                 | [flink][]             | v0.5.0 (deployment tasks)                 |
| [App User](https://github.com/michaelshobbs/dokku-app-user)                                       | [michaelshobbs][]     | v0.7.1 (herokuish 0.3.18)                 |
| [Bower/Grunt](https://github.com/thrashr888/dokku-bower-grunt-build-plugin)                       | [thrashr888][]        | v0.5.0 (deployment tasks and .buildpacks) |
| [Bower/Gulp](https://github.com/gdi2290/dokku-bower-gulp-build-plugin)                            | [gdi2290][]           | v0.5.0 (deployment tasks and .buildpacks) |
| [Bower install](https://github.com/alexanderbeletsky/dokku-bower-install)                         | [alexanderbeletsky][] | v0.5.0 (deployment tasks and .buildpacks) |
| [Bower/Gulp](https://github.com/jagandecapri/dokku-bower-gulp-build-plugin)                       | [jagandecapri][]      | v0.5.0 (deployment tasks and .buildpacks) |
| [Builders: bower, compass, gulp, grunt](https://github.com/ignlg/dokku-builders-plugin)           | [ignlg][]             | v0.5.0 (deployment tasks and .buildpacks) |
| [Custom Domains](https://github.com/neam/dokku-custom-domains)                                    | [neam][]              | v0.3.10 (domains plugin)                  |
| [Debug](https://github.com/josegonzalez/dokku-debug)                                              | [josegonzalez][]      | v0.3.9 (trace command)                    |
| [Dockerfile custom path](https://github.com/mimischi/dokku-dockerfile)                            | [mimischi][]          | v0.25.0 (monorepo support)                |
| [Docker Options](https://github.com/dyson/dokku-docker-options)                                   | [dyson][]             | v0.3.17 (docker-options plugin)           |
| [Dokku Name](https://github.com/alex-sherwin/dokku-name)                                          | [alex-sherwin][]      | v0.4.2 (named containers plugin)          |
| [Events Logger](https://github.com/alessio/dokku-events)                                          | [alessio][]           | v0.3.21 (events plugin)                   |
| [Fonts](https://github.com/ollej/dokku-fonts)                                                     | [ollej][]             | v0.5.0 (deployment tasks)                 |
| [git rev-parse HEAD in env](https://github.com/dokku-community/dokku-git-rev)                     | [cjblomqvist][]       | v0.12.0 (enhanced core git plugin)        |
| [Host Port binding](https://github.com/stuartpb/dokku-bind-port)                                  | [stuartpb][]          | v0.3.17 (docker-options plugin)           |
| [Link Containers](https://github.com/rlaneve/dokku-link)                                          | [rlaneve][]           | v0.3.17 (docker-options plugin)           |
| [List Containers](https://github.com/josegonzalez/dokku-list)                                     | [josegonzalez][]      | v0.3.14 (ps plugin)                       |
| [Logspout](https://github.com/michaelshobbs/dokku-logspout)                                       | [michaelshobbs][]     | v0.22.6 (vector log shipping)             |
| [Long Timeout](https://github.com/investtools/dokku-long-timeout-plugin)                          | [investtools][]       | v0.21.0 (proxy-read-timeout nginx setting)|
| [Monorepo](https://github.com/iamale/dokku-monorepo)                                              | [iamale][]            | v0.25.0 (monorepo builder support)        |
| [Multi-Buildpack](https://github.com/pauldub/dokku-multi-buildpack)                               | [pauldub][]           | v0.4.0 (herokuish)                        |
| [Multiple Domains](https://github.com/wmluke/dokku-domains-plugin)<sup>1</sup>                    | [wmluke][]            | v0.3.10 (domains plugin)                  |
| [Multi Dockerfile](https://github.com/artofrawr/dokku-multi-dockerfile)                           | [artofrawr][]         | v0.25.0 (monorepo support)                |
| [Named-containers](https://github.com/Flink/dokku-named-containers)                               | [flink][]             | v0.4.2 (named-containers plugin)          |
| [Nginx Trust Proxy](https://github.com/kingsquare/dokku-nginx-vhost-trustproxy)                   | [kingsquare][]        | v0.23.0 (nginx x-forwarded-* properties)  |
| [Node](https://github.com/ademuk/dokku-nodejs)                                                    | [ademuk][]            | v0.5.0 (deployment tasks and .buildpacks) |
| [Node](https://github.com/pnegahdar/dokku-node)                                                   | [pnegahdar][]         | v0.5.0 (deployment tasks and .buildpacks) |
| [Nginx-Alt](https://github.com/mikexstudios/dokku-nginx-alt)                                      | [mikexstudios][]      | v0.3.10 (domains plugin)                  |
| [Persistent Storage](https://github.com/dyson/dokku-persistent-storage)                           | [dyson][]             | v0.3.17 (docker-options plugin)           |
| [Pre-Deploy Tasks](https://github.com/michaelshobbs/dokku-app-predeploy-tasks)                    | [michaelshobbs][]     | v0.5.0 (deployment tasks)                 |
| [PrimeCache](https://github.com/darkpixel/dokku-prime-cache)                                      | [darkpixel][]         | v0.3.0 (zero downtime deploys)            |
| [Rollbar](https://github.com/iloveitaly/dokku-rollbar)                                            | [iloveitaly][]        | v0.5.0 (deployment tasks)                 |
| [Syslog](https://github.com/michaelshobbs/dokku-syslog)                                           | [michaelshobbs][]     | v0.22.6 (vector log shipping)             |
| [Haproxy tcp load balancer](https://github.com/256dpi/dokku-haproxy)                              | [256dpi][]            | v0.28.0 (haproxt plugin)                  |
| [Process Manager: Circus](https://github.com/apmorton/dokku-circus)                               | [apmorton][]          | v0.3.14/0.7.0 (ps/restart policy plugin)  |
| [Process Manager: Forego](https://github.com/Flink/dokku-forego)                                  | [flink][]             | v0.3.14/0.7.0 (ps plugin)                 |
| [Process Manager: Forego](https://github.com/iskandar/dokku-forego)                               | [iskandar][]          | v0.3.14/0.7.0 (ps plugin)                 |
| [Process Manager: Logging Supervisord](https://github.com/sehrope/dokku-logging-supervisord)      | [sehrope][]           | v0.3.14/0.7.0 (ps plugin)                 |
| [Process Manager: Shoreman](https://github.com/statianzo/dokku-shoreman)                          | [statianzo][]         | v0.3.14/0.7.0 (ps plugin)                 |
| [Process Manager: Supervisord](https://github.com/statianzo/dokku-supervisord)                    | [statianzo][]         | v0.3.14/0.7.0 (ps plugin)                 |
| [Rebuild application](https://github.com/scottatron/dokku-rebuild)                                | [scottatron][]        | v0.3.14 (ps plugin)                       |
| [Reset mtime](https://github.com/mixxorz/dokku-docker-reset-mtime)                                | [mixxorz][]           | Docker 1.8+                               |
| [SSH Deployment Keys](https://github.com/cedricziel/dokku-deployment-keys)                        | [dokku][]             | v0.33.0 (git plugin)                      |
| [Supply env vars to buildpacks](https://github.com/cameron-martin/dokku-build-env)<sup>2</sup>    | [cameron-martin][]    | v0.3.9 (build-env plugin)                 |
| [Slack Notifications](https://github.com/ribot/dokku-slack)                                       | [ribot][]             | v0.5.0 (deployment tasks)                 |
| [Telegram Notifications](https://github.com/m0rth1um/dokku-telegram)                              | [m0rth1um][]          | v0.5.0 (deployment tasks)                 |
| [user-env-compile](https://github.com/motin/dokku-user-env-compile)<sup>2</sup>                   | [motin][]             | v0.3.9 (build-env plugin)                 |
| [user-env-compile](https://github.com/musicglue/dokku-user-env-compile)<sup>2</sup>               | [musicglue][]         | v0.3.9 (build-env plugin)                 |
| [Volume (persistent storage)](https://github.com/ohardy/dokku-volume)                             | [ohardy][]            | v0.5.0 (storage plugin)                   |
| [Webhooks](https://github.com/nickstenning/dokku-webhooks)                                        | [nickstenning][]      | v0.5.0 (deployment tasks)                 |
| [Wkhtmltopdf](https://github.com/mbriskar/dokku-wkhtmltopdf)                                      | [mbriskar][]          | v0.5.0 (deployment tasks)                 |

<sup>1</sup> Conflicts with [VHOSTS Custom Configuration](https://github.com/neam/dokku-nginx-vhosts-custom-configuration)
<sup>2</sup> Similar to the [heroku-labs feature](https://devcenter.heroku.com/articles/labs-user-env-compile)

### Unmaintained Plugins

The following plugins are no longer maintained by their developers.

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [app-url](https://github.com/mikecsh/dokku-app-url)                                               | [mikecsh][]           | Works with 0.2.0      |
| [Chef cookbooks](https://github.com/fgrehm/chef-dokku)                                            | [fgrehm][]            |                       |
| [CouchDB (multi containers)](https://github.com/Flink/dokku-couchdb-multi-containers)             | [flink][]             | 0.4.0+                |
| [CouchDB](https://github.com/racehub/dokku-couchdb-plugin)                                        | [raceHub][]           | Compatible with 0.2.0 |
| [Dokku Copy App Config Files](https://github.com/alexkruegger/dokku-app-configfiles)              | [alexkruegger][]      | Compatible with 0.3.17+ |
| [Dokku Registry](https://github.com/agco-adm/dokku-registry)                                      | [agco-adm][]          | 0.4.0+
| [Elasticsearch](https://github.com/robv/dokku-elasticsearch)                                      | [robv][]              | Not compatible with >= 0.3.0 (still uses /home/git) |
| [Elasticsearch](https://github.com/blag/dokku-elasticsearch-plugin)<sup>1</sup>                   | [blag][]              | Compatible with 0.2.0 |
| [Graphite/statsd](https://github.com/jlachowski/dokku-graphite-plugin)                            | [jlachowski][]        | < 0.4.0               |
| [HipChat Notifications](https://github.com/cef/dokku-hipchat)                                     | [cef][]               |                       |
| [Memcached](https://github.com/Flink/dokku-memcached-plugin)                                      | [flink][]             | 0.4.0+                |
| [MongoDB (single container)](https://github.com/jeffutter/dokku-mongodb-plugin)                   | [jeffutter][]         |                       |
| [MySQL](https://github.com/hughfletcher/dokku-mysql-plugin)                                       | [hughfletcher][]      |                       |
| [Neo4j](https://github.com/Aomitayo/dokku-neo4j-plugin)                                           | [aomitayo][]          |                       |
| [PostGIS](https://github.com/fermuch/dokku-pg-plugin)                                             | [fermuch][]           |                       |
| [PostgreSQL (single container)](https://github.com/jeffutter/dokku-postgresql-plugin)             | [jeffutter][]         | This plugin creates a single postgresql container that all your apps can use. Thus only one instance of postgresql running (good for servers without a ton of memory). |
| [Redis](https://github.com/luxifer/dokku-redis-plugin)                                            | [luxifer][]           |                       |
| [Redis](https://github.com/sekjun9878/dokku-redis-plugin)                                         | [sekjun9878][]        | 0.3.26+               |
| [RiakCS (single container)](https://github.com/jeffutter/dokku-riakcs-plugin)                     | [jeffutter][]         | Incompatible with 0.2.0 |

<sup>1</sup> Forked from [jezdez/dokku-elasticsearch-plugin](https://github.com/jezdez/dokku-elasticsearch-plugin): uses Elasticsearch 1.2 (instead of 0.90), doesn't depend on dokku-link, runs as elasticsearch user instead of root, and turns off multicast autodiscovery for use in a VPS environment.

[256dpi]: https://github.com/256dpi
[ademuk]: https://github.com/ademuk
[agco-adm]: https://github.com/agco-adm
[alessio]: https://github.com/alessio
[alex-sherwin]: https://github.com/alex-sherwin
[alexanderbeletsky]: https://github.com/alexanderbeletsky
[alexkruegger]: https://github.com/alexkruegger
[aluxian]: https://github.com/aluxian
[andrew-womeldorf]: https://github.com/andrew-womeldorf
[aomitayo]: https://github.com/aomitayo
[apmorton]: https://github.com/apmorton
[artofrawr]: https://github.com/artofrawr
[AxelTheGerman]: https://github.com/AxelTheGerman
[badsyntax]: https://github.com/badsyntax
[basgys]: https://github.com/basgys
[benjamin-dobell]: https://github.com/benjamin-dobell
[blag]: https://github.com/blag
[calyhre]: https://github.com/calyhre
[cameron-martin]: https://github.com/cameron-martin
[candlewaster]: https://notabug.org/candlewaster
[cedricziel]: https://github.com/cedricziel
[cef]: https://github.com/cef
[cjblomqvist]: https://github.com/cjblomqvist
[crisward]: https://github.com/crisward
[cu12]: https://github.com/cu12
[darkpixel]: https://github.com/darkpixel
[dokku]: https://github.com/dokku
[dokku-community]: https://github.com/dokku-community
[dyson]: https://github.com/dyson
[fermuch]: https://github.com/fermuch
[fgrehm]: https://github.com/fgrehm
[flink]: https://github.com/flink
[fomojola]: https://github.com/fomojola
[gdi2290]: https://github.com/gdi2290
[hughfletcher]: https://github.com/hughfletcher
[iamale]: https://github.com/iamale
[ignlg]: https://github.com/ignlg
[iloveitaly]: https://github.com/iloveitaly
[investtools]: https://github.com/investtools
[iskandar]: https://github.com/iskandar
[jagandecapri]: https://github.com/jagandecapri
[jeffutter]: https://github.com/jeffutter
[jlachowski]: https://github.com/jlachowski
[josegonzalez]: https://github.com/josegonzalez
[kingsquare]: https://github.com/kingsquare
[kloadut]: https://github.com/kloadut
[krisrang]: https://github.com/krisrang
[luxifer]: https://github.com/luxifer
[m0rth1um]: https://github.com/m0rth1um
[maciej łebkowski]: https://github.com/mlebkowski
[mainto]: https://github.com/mainto
[matto1990]: https://github.com/matto1990
[mbreit]: https://github.com/mbreit
[mbriskar]: https://github.com/mbriskar
[michaelshobbs]: https://github.com/michaelshobbs
[mikecsh]: https://github.com/mikecsh
[mikexstudios]: https://github.com/mikexstudios
[mimischi]: https://github.com/mimischi
[mixxorz]: https://github.com/mixxorz
[motin]: https://github.com/motin
[mrname]: https://github.com/mrname
[musicglue]: https://github.com/musicglue
[neam]: https://github.com/neam
[nickcharlton]: https://github.com/nickcharlton
[nickstenning]: https://github.com/nickstenning
[ohardy]: https://github.com/ohardy
[pauldub]: https://github.com/pauldub
[pnegahdar]: https://github.com/pnegahdar
[racehub]: https://github.com/racehub
[ribot]: https://github.com/ribot
[rlaneve]: https://github.com/rlaneve
[robv]: https://github.com/robv
[scottatron]: https://github.com/scottatron
[sehrope]: https://github.com/sehrope
[sekjun9878]: https://github.com/sekjun9878
[statianzo]: https://github.com/statianzo
[stuartpb]: https://github.com/stuartpb
[Tashows]: https://github.com/Tashows
[thrashr888]: https://github.com/thrashr888
[wmluke]: https://github.com/wmluke
[zenedith]: https://github.com/zenedith
[fteychene]: https://github.com/fteychene
[baikunz]: https://github.com/baikunz
[lazyatom]: https://github.com/lazyatom
[ollej]: https://github.com/ollej
[ignisda]: https://github.com/IgnisDa
