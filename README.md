# htaccess-for-google-speed
```apacheconf
<IfModule mod_headers.c>

	<FilesMatch "\.(js|css)$">
		Header set Cache-Control "max-age=31536000"
	</FilesMatch>

	<FilesMatch "\.(svg|ico|gif|jpg|jpeg|png)$">
		Header set Cache-Control "max-age=31536000"
	</FilesMatch>

	<FilesMatch "\.(ttf|woff|woff2|otf)$">
		Header set Cache-Control "max-age=31536000"
	</FilesMatch>

</IfModule>

<ifModule mod_expires.c>
	ExpiresActive On

	ExpiresByType image/x-icon "access plus 1 year"
	ExpiresByType image/jpeg "access plus 1 year"
	ExpiresByType image/png "access plus 1 year"
	ExpiresByType image/gif "access plus 1 year"
	ExpiresByType image/svg "access plus 1 year"
	ExpiresByType image/svg+xml "access plus 1 year"

	ExpiresByType application/x-font-ttf "access plus 1 year"
	ExpiresByType application/x-font-truetype "access plus 1 year"
	ExpiresByType application/x-font-otf "access plus 1 year"
  	ExpiresByType application/x-font-woff "access plus 1 year"
	ExpiresByType application/x-font-woff2 "access plus 1 year"

	ExpiresByType text/css "access plus 1 year"
	ExpiresByType text/javascript "access plus 1 year"
	ExpiresByType application/javascript "access plus 1 year"
	ExpiresByType application/x-javascript "access plus 1 year"

</ifModule>
```
