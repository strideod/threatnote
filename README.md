![img](https://i.imgur.com/xqc8bGL.png)

## Getting Started

Check out the docs at <https://docs.threatnote.io/> to get started!

## Quick Start

First you'll want to clone the threatnote.io repo

```bash
git clone git@github.com:brianwarehime/threatnote.git 
cd threatnote/threatnote
cp env_example env
vi env (change the secret key)
add 0.0.0.0 local.docker to your /etc/hosts file
docker build . --tag threatnote 
docker-compose up
```

This will launch the following:

- Flask app running threatnote.io listening on port 5000 (access <http://local.docker:5000> to login)
- Redis server to manage Redis workers
- A Redis worker named enricher to manage the enrichment jobs

To stop threatnote.io, just run:
`$ docker-compose down`

To login, use admin@threatnote.io and admin as your credentials

For a general overview of the product, check out <https://threatnote.io>
