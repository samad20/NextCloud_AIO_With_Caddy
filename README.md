# Pull needed images

    docker pull nextcloud/all-in-one:lateste
    docker pull nextcloud/aio-nextcloud:latest
    docker pull nextcloud/aio-collabora:latest
    docker pull nextcloud/aio-domaincheck:latest
    docker pull nextcloud/aio-imaginary:latest
    docker pull nextcloud/aio-postgresql:latest
    docker pull nextcloud/aio-redis:latest
    docker pull nextcloud/aio-talk:latest
    docker pull nextcloud/aio-apache:latest
# Install Caddy

 [Read this web page ](https://caddyserver.com/docs/install)

# Caddyfile configuration
configure your caddyfile

    sudo nano /etc/caddy/Caddyfile


If you want use domain name your Caddyfile should look like this:

    yourdamin {
           reverse_proxy localhost:11000 
        }

If you want use local domain (only work in your local network), your Caddyfile should look like this:

    yourdamin.local {
           reverse_proxy localhost:11000 
        }
