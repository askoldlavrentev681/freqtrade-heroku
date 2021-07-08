Creating the app
```shell
git clone https://github.com/joaorafaelm/freqtrade.git && cd freqtrade
heroku update beta
heroku plugins:install @heroku-cli/plugin-manifest
heroku create --manifest
heroku labs:enable runtime-dyno-metadata
heroku addons:create securekey
heroku dyno:scale web=1
```

Set environment variables
```
# example: heroku config:set KEY=value

```

Deploying
```
git push heroku master
```

Open [FreqUI](https://github.com/freqtrade/frequi)
```
heroku open
```

Edit `Procfile` to add or remove bots.
