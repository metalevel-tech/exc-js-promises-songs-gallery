# Command-line

Here is a list of my custom scrips, commands and procedures, related to the app deployment.

## Reverse proxy for the app

```bash
sudo a2proxy 'songsg' '48002'
```

```bash
sudo a2proxy 'songsg' remove
```

## Docker container for the app

```bash
# docker run -p '48002':'48002' 'songsg' -d
```

```bash
docker-compose up -d
```

```bash
docker-compose down
```

```bash
docker-prune.sh
```

## [PM2](https://www.npmjs.com/package/pm2) service for the app

```bash
cd app/
npm install
```

```bash
pm2 start 'npm run watch' --name 'songsg'
pm2 save
```

```bash
pm2 start 'npm start' --name 'songsg'
pm2 save
```

```bash
pm2 stop 'songsg'
pm2 delete 'songsg'
pm2 save
```
