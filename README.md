https://itsfoss.com/connect-wifi-terminal-ubuntu/
https://askubuntu.com/questions/1260753/no-wifi-networks-listed-ubuntu-20-04-broadcom-bcm4360
https://medium.com/soulweb-academy/docker-local-dev-stack-with-traefik-https-dnsmasq-locally-trusted-certificate-for-ubuntu-20-04-5f036c9af83d

docker network create traefik
chmod 600 traefik/acme.json

```bash
# If it's the firt install of mkcert, run
mkcert -install

# Generate certificate for domain "docker.localhost", "domain.local" and their sub-domains
mkcert -cert-file certs/local-cert.pem -key-file certs/local-key.pem "docker.localhost" "*.docker.localhost" "domain.local" "*.domain.local"
```