# Nextcloud Docker Setup

1. Configure `docker-compose.yml`
2. Configure `db.env`
3. Run `docker-compose up -d`
4. Configure `example.com.conf` and rename to the domain to be used for the installation
5. Move `example.com.conf` to `/etc/nginx/sites-available/`
6. Run `sudo ln -s /etc/nginx/sites-available/example.com.conf /etc/nginx/sites-enabled/example.com.conf`
7. Run `sudo nginx -t` to check that the config is good
8. Run `sudo systemctl restart nginx`
9. Install Letsencrypt certificates using `sudo certbot --nginx`
