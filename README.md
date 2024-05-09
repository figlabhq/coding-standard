# FIGLAB Coding Standard

PHPCS coding-standard for Laravel applications and packages. Based on the awesome [IxDF Coding Standard](https://github.com/InteractionDesignFoundation/coding-standard/).

## Installation

1. Install the package via composer by running:
```shell
composer require --dev figlab/coding-standard
```

2. Add composer scripts into your `composer.json`:
```json
"scripts": {
  "cs:check": "phpcs -p -s --colors --report-full --report-summary",
  "cs:fix": "phpcbf -p --colors"
}
```

3. Create file `phpcs.xml` on base path of your repository with content
```xml
<?xml version="1.0"?>
<ruleset name="My Coding Standard">
    <!-- Include all rules from the IxDF Coding Standard -->
    <rule ref="FigLabCodingStandard"/>

    <!-- Paths to check -->
    <file>app</file>
    <file>config</file>
    <file>database</file>
    <file>lang</file>
    <file>routes</file>
    <file>tests</file>
</ruleset>
```

## Usage

- To run checks only:

```shell
composer cs:check
```

- To automatically fix CS issues:

```shell
composer cs:fix
```
