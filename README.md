# php-vendors-cleanup

Clear php vendor-dir from unwanted files

Script removes:
 - tests and related files
 - docs
 - composer files
 - all dotfiles
 - Symfony's WebProfilerBundle and DebugBundle which are not needed in production environment
 - Symfony's Intl data

# Why?

On typical Symfony installation we have about ~10k files
```
$ find vendor -type f | wc -l
   12843
```

But a big part of them is not required in production environment and may be removed
```
$ ./vendor/bin/clear_vendors
$ find vendor -type f | wc -l
   5579
```

## Usage

```
composer require sc0/vendors-cleanup
./vendors/bin/clear_vendors
```
