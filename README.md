# docker-TechnitiumSoftware-DnsServer

## Setup
<details>
  <summary>Compose</summary>

```yml
  dnsserver:     
    container_name: ts-dnsserver
    image: roxedus/ts-dnsserver:latest
    ports:
      - 53:53
      - 5380:5380
    volumes:
      - ./ts-dnsserver:/config
    environment:
      - PUID=1000
      - PGID=1000
```
  
</details>