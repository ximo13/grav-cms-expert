# Troubleshooting

## Cache Permission Error

Error:

```text
Failed to save file cache/compiled/...
```

Cause:

* Incorrect permissions on cache directories.

Fix:

```bash
sudo chown -R www-data:www-data cache logs tmp
sudo chmod -R 775 cache logs tmp
php bin/grav clear-cache
```

## Theme Not Visible In Admin

Check:

* blueprints.yaml
* slug-matching theme configuration file
* clear Grav cache
* theme folder structure
