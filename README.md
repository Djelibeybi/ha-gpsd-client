# GPSD Client for Home Assistant

This component will set up a `sensor` platform that contains the current location
and time data from an external `gpsd` instance.

## Installation

1. Add <https://github.com/Djelibeybi/ha-gpsd-client> as a custom `integration`
   repository in [HACS][HACS].
2. Add at least the following to `configuration.yaml` :

```yaml
sensor:
  - platform: gpsd_client
    name: GPSD Client
```

By default, the integration looks for GPSD on `localhost` on port `2947`. If your
`gpsd` server is on a different host, you must configure the the `host` and `port`:

```yaml
sensor:
  - platform: gpsd_client
    name: GPSD Client
    host: remote-gpsd.example.com
    port: 12345
```

***

[HACS]: https://hacs.xys
