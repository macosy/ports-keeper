# Ports Keeper

Hence, we can find port mapped services easily ~ :100:

# Stacks

  - [dnsmasq](#dnsmasq)
  - [nginx](#nginx)

# Setup 

```
  brew install dnsmasq nginx
```

then edit relevant configs in `conf`

## dnsmasq

* start service with sudo priviledges
* verification: `python -m http.server 8888`, and curl the domain ex:
'curl something.sample:8888` should not return error.

## nginx 

* start service with sudo priviledges (port 80 requires permissions)

# Usage

## Add TLD

    * step 1: add `nameserver 127.0.0.1` in `/etc/resolver/[tld]`
    * step 2: add/update `address=/[tld]/127.0.0.1` in `conf/dnsmasq`
    * step 3: add/update upstream blocks in `servers/[tld]`
    * step 4: ./sync 
    * step 5: restart nginx

## Add sub domain

    * step 1: add/update upstream blocks in `servers/[tld]`
    * step 2: restart nginx

Note: ensure newly added services only expose to localhost interface as a good
practice.

# Ref

- https://gist.github.com/brandonblack/ee81745569ae98306555f108bf69ff5c

## Versions

```
> brew info nginx dnsmasq | grep 'nginx:\|dnsmasq:'
nginx: stable 1.13.10 (bottled), HEAD
dnsmasq: stable 2.79 (bottled)
```

### Alternatives

- [POW](http://pow.cx/manual.html)

