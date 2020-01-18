# [docker-TechnitiumSoftware-DnsServer](https://github.com/Roxedus/docker-TS-DnsServer)

[Technitium DNS Server](https://github.com/TechnitiumSoftware/DnsServer) is an open source tool that can be used for self hosting a local DNS server for privacy & security or, used for experimentation/testing by software developers on their computer. It works out-of-the-box with no or minimal configuration and provides a user friendly web console accessible using any web browser.

## Setup

<details>
  <summary>Compose example</summary>

```yml
  dnsserver:
    container_name: ts-dnsserver
    image: roxedus/ts-dnsserver:latest
    ports:
      - 53:53/udp
      - 5380:5380
    volumes:
      - ${PWD}/ts-dnsserver:/config
    environment:
      - PUID=1000
      - PGID=1000
```

</details>
<details>
  <summary>Docker run example</summary>

```bash
docker run -p 53:53/udp -p 5380:5380 -v ${PWD}/ts-dnsserver:/config -e PUID=1000 -e PGID=1000 roxedus/ts-dnsserver:latest
```

</details>
