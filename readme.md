# Mocking Lot

Hence, we can find mockings asap~

# Stack

  - [dnsmasq](#dnsmasq)
  - [nginx](#nginx)

# Setup 

```
  brew install dnsmasq nginx
```

## dnsmasq

* start service with sudo priviledges
* verification: `python -m http.server 8888`, and curl the domain ex:
'curl something.sample:8888` should not return error.

## nginx 

* start service with sudo priviledges (port 80 requires permissions)

# Ref

- https://gist.github.com/brandonblack/ee81745569ae98306555f108bf69ff5c

## Versions

```
> brew info nginx dnsmasq | grep 'nginx:\|dnsmasq:'
nginx: stable 1.13.10 (bottled), HEAD
dnsmasq: stable 2.79 (bottled)
```

### Alternatives

- POW

