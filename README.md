# php-vendors-cleanup

Clear php vendor-dir from unwanted files

Script removes:
 - tests and related files
 - docs
 - composer files
 - all dotfiles
 - Symfony's WebProfilerBundle and DebugBundle which are not needed in production environment
 - Symfony's Intl data

## Usage

`composer require sc0/vendors-cleanup --no-dev`
`./vendors/bin/clear_vendors`
