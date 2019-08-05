# Nextcloud Docker Setup

1. Configure `docker-compose.yml`
2. Configure `db.env`
3. Configure `example.com.conf` and rename to the domain to be used for the installation
4. Move `example.com.conf` to `/etc/nginx/sites-available/`
5. Run `sudo ln -s /etc/nginx/sites-available/example.com.conf /etc/nginx/sites-enabled/example.com.conf`
6. Run `sudo nginx -t` to check that the config is good
7. Run `sudo systemctl restart nginx`
8. Install Letsencrypt certificates using `sudo certbot --nginx`
