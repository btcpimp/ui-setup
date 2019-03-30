# ui-setup
Tool for quick deployment of golos-classic web client.

## Setup

1. Clone this repo:  
```
git clone git@github.com:golos-classic/ui-setup.git && cd ui-setup
```

2. Generate a new crypto_key and save under server_session_secret in config.json.
```
openssl rand -base64 32
```

3. Migrapte database:  
```
docker-compose run --rm web bash -c "cd db && sequelize db:migrate"
```

4. Run services:  
```
docker-compose up -d
```

Done! Access your instance at ```localhost:9000```

## TODO
1. Fix some mysql errors.
