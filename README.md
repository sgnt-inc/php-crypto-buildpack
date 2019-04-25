Simple Heroku buildpack to compile and install the Crypto extension for OpenSSL
bindings. (https://github.com/bukka/php-crypto)

The extension requires a `composer.json` to be present in the root directory to be 
detected as a php app.

The buildpack installs the extension using PECL (https://pecl.php.net/package/crypto)

The buildpack enables the extension by writing `extension=crypto.so` to 
`/app/.heroku/php/etc/php/conf.d/20-crypto.ini`
