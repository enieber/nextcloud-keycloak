# Nextcloud development environment

An development apps environment for Nextcloud.

## Development environment

### Before first run

Copy `.env.example` to `.env` and change the values of `.env`

`VERSION_NEXTCLOUD` To this environment get a or branch of [Nextcloud server repository](github.com/nextcloud/server).

### PHP custom settings

If you need custom settings in PHP, change the file [`.docker/app/config/php.ini`](/.docker/app/config/php.ini).

### Up environment
```bash
docker-compsoe up -d
```
Access in the browser using the port defined on `HTTP_PORT`.

After finish the setup, access this url: http://localhost/settings/admin/overview.

## Start development

Follow the instructions in official Nextcloud app development page.

After create the folder to your app, in terminal, change the owner of the folder to your user:

```bash
sudo chown -R $USER:$USER nextcloud/apps/yourappfolder
```

Go to your app folder and initialize versioning.

```php
cd nextcloud/apps/yourappfolder
```

Good work!