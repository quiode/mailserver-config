# mailserver-config

docker compose config for my mail server

## Cronjob

*as sudo*  
`0 4 * * * docker run --rm -it -v "/docker-data/certbot/certs/:/etc/letsencrypt/" -v "/docker-data/certbot/logs/:/var/log/letsencrypt/" -p 80:80 -p 443:443 certbot/certbot renew`

## User

- <mail@dominik-schwaiger.ch>
- <nextcloud@dominik-schwaiger.ch>
- <gitlab@dominik-schwaiger.ch>

## DNS-Config

- MX to dominik-schwaiger.vsos.ethz.ch
- _dmarc.dominik-schwaiger.ch to  "v=DMARC1; p=none; rua=mailto:nextcloud@dominik-schwaiger.ch,mailto:gitlab@dominik-schwaiger.ch,mailto:mail@dominik-schwaiger.ch; ruf=mailto:mail@dominik-schwaiger.ch; sp=none; fo=1; ri=86400"
- mail._domainkey.dominik-schwaiger.ch to  "v=DKIM1;h=sha256;k=rsa;p=MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAyRn1qFnIA3mVeZz9ukTshYSgPAhxb9MaxVENkAYzikZcDBq68bTH7mQRpKD7TfZZ6g4qyuHlwIhJhMc3FbJiuG7SqVTmDGbDMZl61oT9+t7LaW7cf91R6AH8HPGKL9X4PRZoZ6x6Mq5MwaIQHjDJQ3KDN3CWcfQxrF7P9yQ44czDZnFPXs8EKpVPniWzt+N9no5GCLobFWgd4P1ZmtNCJNJ4tm1ScmJeslzQ7FZIoHXQOISdWKTED0KE0mtuzW3EVOWO3o4prY57CvyZ8rlO/Cw2c7Wde+UeQ58eYS6u1aOT1eFtsj0ROevK7eaKpEJVtGo3oObTSTIMztvVNbciYQIDAQAB"
