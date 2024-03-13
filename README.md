# mailserver-config
docker compose config for my mail server

## Cronjob
*as sudo*  
`0 4 * * * docker run --rm -it -v "${PWD}/docker-data/certbot/certs/:/etc/letsencrypt/" -v "${PWD}/docker-data/certbot/logs/:/var/log/letsencrypt/" -p 80:80 -p 443:443 certbot/certbot renew`

## User
- mail@dominik-schwaiger.ch
- nextcloud@dominik-schwaiger.ch

## DNS-Config
- MX to dominik-schwaiger.vsos.ethz.ch