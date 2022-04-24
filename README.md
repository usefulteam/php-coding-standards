# Useful Coding Standards

These are a set of modern (PHP *8+*) linting guidelines for general PHP development.

These guidelines are developed heavily based on [Neutron PHP Standard](https://github.com/Automattic/phpcs-neutron-standard) and [Inpsyde PHP Coding Standards](https://github.com/inpsyde/php-coding-standards), but without the WordPress specific.

This project is a [phpcs](https://github.com/squizlabs/PHP_CodeSniffer) "standard" (a collection of rules or "sniffs") that can be included in any PHP project.

## Installation

To use these rules in a project which is set up using [composer](https://href.li/?https://getcomposer.org/), we recommend using the [phpcodesniffer-composer-installer library](https://href.li/?https://github.com/DealerDirect/phpcodesniffer-composer-installer) which will automatically use all installed standards in the current project with the composer type `phpcodesniffer-standard` when you run phpcs.

```
composer require --dev squizlabs/php_codesniffer dealerdirect/phpcodesniffer-composer-installer
composer require --dev usefulteam/php-coding-standards
```

## Configuration

When installing sniff standards in a project, you edit a `phpcs.xml` file with the `rule` tag inside the `ruleset` tag. The `ref` attribute of that tag should specify a standard, category, sniff, or error code to enable. It’s also possible to use these tags to disable or modify certain rules. The [official annotated file](https://href.li/?https://github.com/squizlabs/PHP_CodeSniffer/wiki/Annotated-ruleset.xml) explains how to do this.

```xml
<?xml version="1.0"?>
<ruleset name="MyStandard">
 <description>My library.</description>
 <rule ref="UsefulCodingStandards"/>
</ruleset>
```

## Usage

Most editors have a phpcs plugin available, but you can also run phpcs manually. To run phpcs on a file in your project, just use the command-line as follows (the `-s` causes the sniff code to be shown, which is very important for learning about an error).

```
vendor/bin/phpcs -s src/MyProject/MyClass.php 
```

-----

# Guidelines

View the Guidelines [here](./GUIDELINES.md).