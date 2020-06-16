# CoturnTemplate
A Coturn STUN/TURN server template using Docker.


## Prerequisites
* You must use this template on a machine with letsencrypt https certificates.
* The machine should have docker and docker-compose installed.
* If you're using a firewall make sure to have the following rules:
```
To                         Action      From
--                         ------      ----

3478/tcp                   ALLOW       Anywhere                   # TURN server
5349/tcp                   ALLOW       Anywhere                   # TURN server (Secure)
49152:65535/udp            ALLOW       Anywhere                   # Multimedia ports
3478/udp                   ALLOW       Anywhere                   # UDP TURN server
5349/udp                   ALLOW       Anywhere                   # UDP TURN server (Secure)
3478/tcp (v6)              ALLOW       Anywhere (v6)              # TURN server
5349/tcp (v6)              ALLOW       Anywhere (v6)              # TURN server (Secure)
49152:65535/udp (v6)       ALLOW       Anywhere (v6)              # Multimedia ports
3478/udp (v6)              ALLOW       Anywhere (v6)              # UDP TURN server
5349/udp (v6)              ALLOW       Anywhere (v6)              # UDP TURN server (Secure)
```

# REMEMBER:
* Before you run this thing, make sure you create a turnserver.conf file. Copy the turnserver.conf.sample file.

## Run It!
Just execute the following at the root of this repo.
```
$ docker-compose up -d;
```

