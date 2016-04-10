# Joomla CMS Information
All information about managing Joomla website

##Get Joomal version via command line :

1. For Cpanel : 
```bash
find /home/*/public_html/ -type f \( -iwholename '*/libraries/joomla/version.php' -o -iwholename '*/libraries/cms/version.php' -o -iwholename '*/libraries/cms/version/version.php' \) -print0 -exec perl -e 'while (<>) { $release = $1 if m/ \$RELEASE\s+= .([\d.]+).;/; $dev = $1 if m/ \$DEV_LEVEL\s+= .(\d+).;/; } print qq( = $release.$dev\n);' {} \;
```
2. For Plesk :
```bash
find /var/www/vhosts/*/httpdocs -type f \( -iwholename '*/libraries/joomla/version.php' -o -iwholename '*/libraries/cms/version.php' -o -iwholename '*/libraries/cms/version/version.php' \) -print0 -exec perl -e 'while (<>) { $release = $1 if m/ \$RELEASE\s+= .([\d.]+).;/; $dev = $1 if m/ \$DEV_LEVEL\s+= .(\d+).;/; } print qq( = $release.$dev\n);' {} \;
```
