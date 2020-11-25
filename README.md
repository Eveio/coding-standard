# eve Coding Standard

[eve](https://eve.io)'s coding standard for [PHP CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer), built on top of [slevomat/coding-standard](https://github.com/slevomat/coding-standard).

## Installation

Require the package with Composer:

```bash
composer require --dev eve/coding-standard
```

## Usage

1. In your `ruleset.xml`, add a rule referencing the package's included rule set:

    ```xml
    <?xml version="1.0"?>
    <ruleset name="My Awesome Standards">
        <rule ref="./vendor/eve/coding-standard/ruleset.xml"/>

        <!-- add extra configurations if necessary -->
        <file>./app</file>
        <file>./bootstrap</file>
        <file>./config</file>
        <file>./database</file>
        <file>./routes</file>
        <file>./tests</file>
    </ruleset>
    ```

1. Use it!

    ```bash
    # check for violations
    composer phpcs --standard=ruleset.xml
   
    # fix the violations if applicable
    composer phpcbf --standard=ruleset.xml 
    ```

## License

MIT of course.
