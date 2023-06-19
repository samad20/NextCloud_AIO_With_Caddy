# Install NextCloud AIO using docker-compose and caddy

![enter image description here](https://upload.wikimedia.org/wikipedia/commons/thumb/6/60/Nextcloud_Logo.svg/160px-Nextcloud_Logo.svg.png)

## Pull needed images

    docker pull nextcloud/all-in-one:lateste
    docker pull nextcloud/aio-nextcloud:latest
    docker pull nextcloud/aio-collabora:latest
    docker pull nextcloud/aio-domaincheck:latest
    docker pull nextcloud/aio-imaginary:latest
    docker pull nextcloud/aio-postgresql:latest
    docker pull nextcloud/aio-redis:latest
    docker pull nextcloud/aio-talk:latest
    docker pull nextcloud/aio-apache:latest
## Install Caddy

 [Read this web page ](https://caddyserver.com/docs/install)

## Caddyfile configuration
configure your caddyfile

    sudo nano /etc/caddy/Caddyfile


If you want use domain name your Caddyfile should look like this:

    yourdamin {
           reverse_proxy localhost:11000 
        }

        
     
## Install Nextcloud AIO

Clone the repository

    git clone https://github.com/samad20/NextCloud_AIO_With_Caddy.git

Change directory 

    cd NextCloud_AIO_With_Caddy
Create and start containers

    docker compose up -d
Open  `https://localhost:8080` and complete installation process.

After that, you can access nextcloud by `https://your_domain`.
