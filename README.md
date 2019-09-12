# htaccessory
.htaccess help


Restrict wordpress login to certain ip's
```
<IfModule mod_rewrite.c>
RewriteEngine on
RewriteCond %{REQUEST_URI} ^(.*)?wp-login\.php(.*)$ [OR]
RewriteCond %{REQUEST_URI} ^(.*)?wp-admin$
RewriteCond %{REMOTE_ADDR} !^123.456.789.012$
RewriteCond %{REMOTE_ADDR} !^123.456.789.013$
RewriteCond %{REMOTE_ADDR} !^123.456.789.014$
RewriteRule ^(.*)$ - [R=403,L]
</IfModule>
```
