# Altibox

Command line interface to your Altibox router.  
(Work in progress, currently only support listing connected devices)

```
Usage: ./altibox.pl [options]
```

## Global options

```
--command <command>
--user <user>
--password <password>
[--verbose]
```

## Commands

### Devices (--command devices)

```
--command devices
[--format <raw|influxdb|table>]
[--output <file>]
[--loop <seconds>]
```

```
$ ./altibox.pl --command devices --user foo@bar.zot --password xxxyyyzzz
Name        MAC               IP             Connection RSSI
rockrobo    34:ce:00:e9:a2:73 192.168.10.191 WIFI24GHZ  65
Laptop      f0:4d:a2:c1:11:00 192.168.10.187 WIFI5GHZ   45
raspberrypi dc:a6:32:1c:7b:9f 192.168.10.182 WIFI5GHZ   62
Apple-TV    90:dd:5d:cb:f2:3b 192.168.10.139 WIRED       0
```

Environment variables can be used for all options: `ALTIBOX_COMMAND`, `ALTIBOX_USER`, `ALTIBOX_PASSWORD`, `ALTIBOX_FORMAT`, `ALTIBOX_OUTPUT`, `ALTIBOX_LOOP`, `ALTIBOX_VERBOSE`.

## Docker

A docker image is available [here](https://github.com/users/terjesannum/packages/container/package/altibox).
