# Grocy dev server

This repo allows you to set up a development server for [Grocy](https://grocy.info/). You are able to test on mobile device due to enable TLS on port 8443.

Make sure, the current user is part of the `www-data` user group and you have docker-compose installed.

Usage:
```bash
# Enter the path, where you wan't to setup the dev system.
cd dev
# Clone grocy
git clone https://github.com/grocy/grocy.git
# Clone dev server
git clone https://github.com/Mik-/grocy-dev-server.git
# Create viewcache folder
mkdir grocy/data/viewcache
# Copy config
cp grocy/config-dist.php grocy/data/config.php
# Make data folder accessible by the dev server
chown -R www-data:www-data grocy/data
# Start the server
cd grocy-dev-server
docker-compose up
```