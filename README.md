# Cron Daemon

This image lets you run scripts using cron daemon. You should extend this
image by adding tools you need, like rsync, ssh, ncat or others.


## Using

You should mount a folder with your scripts in crond container. The folders
watched by cron daemon are:

* /etc/periodic/15min
* /etc/periodic/hourly
* /etc/periodic/daily
* /etc/periodic/weekly
* /etc/periodic/monthly


## Example

```
docker run --rm -name crontainer \
           -v /my-hourly-scripts/:/etc/periodic/hourly \
           -d montefuscolo/crond
```

