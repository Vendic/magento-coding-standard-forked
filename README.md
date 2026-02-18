# Magento Coding Standard

A set of Magento rules for [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) tool.

## Installation within a Magento 2 site

To use within your Magento 2 project you can use:

```bash
composer require --dev magento/magento-coding-standard
```

Due to security, when installed this way the Magento standard for phpcs cannot be added automatically.
You can achieve this by adding the following to your project's `composer.json`:

```json
"scripts": {
    "post-install-cmd": [
      "([ $COMPOSER_DEV_MODE -eq 0 ] || vendor/bin/phpcs --config-set installed_paths ../../magento/magento-coding-standard/)"
    ],
    "post-update-cmd": [
      "([ $COMPOSER_DEV_MODE -eq 0 ] || vendor/bin/phpcs --config-set installed_paths ../../magento/magento-coding-standard/)"
    ]
}
```

## Changes

Here's a list of changes done by Vendic for original package

### Code Sniffer testVersion

Phpcs test version was changed in ruleset.xml to match fresh supported PHP (8.3-8.4)